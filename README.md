# Multi-Scale Temperature Converter

**Problem Statement:**
Create a program that converts temperatures between Celsius, Fahrenheit, and Kelvin scales. The program should prompt the user to input a temperature value and the original unit of measurement. It should then convert the temperature to the other two units and display the converted values to the user. For example, if the user enters a temperature of 25 degrees Celsius, the program should convert it to Fahrenheit and Kelvin, and present the converted values as the outputs.

**Procedure:**
1. Enter temperature and unit, then click "Convert" for instant conversion.
2. View the converted temperature values in Celsius, Fahrenheit, and Kelvin.
3. Optionally, reset the form to clear input fields and hide the result.
4. Repeat the process as needed for multiple temperature conversions.
5. Interface streamlines temperature conversions for quick and easy use.

**Technologies Used:**
1. HTMl
2. CSS
3. JAVA SCRIPT
4. Python

**Preview:**

![image](https://github.com/SasankSami21/PRODIGY_SD_01/assets/112636647/cff893a3-38e1-4c45-ac69-facb1263757a)

Function GenerateDAG(epoch):
    size = CalculateDAGSize(epoch)  // Calculate size based on epoch
    DAG = CreateNewDAG(size)         // Create a new DAG
    StoreDAGInMemory(DAG)             // Store DAG in miner's memory
    Return DAG

Function MixData(blockHeader, nonce, DAG):
    mixHash = Hash(blockHeader + nonce)  // Create initial mix hash
    dataChunks = FetchDataFromDAG(DAG, mixHash)  // Retrieve data from DAG
    Return dataChunks

Function HashData(dataChunks):
    mixHash = InitialMixHash()  // Initialize mix hash
    For each chunk in dataChunks:
        mixHash = Keccak256(mixHash + chunk)  // Hash each chunk with mix hash
    Return mixHash

Function VerifyAndSubmitBlock(block, minerID, difficultyThreshold):
    mixHash = HashData(MixData(block.header, block.nonce, DAG))  // Hashing process
    If mixHash < difficultyThreshold:  // Check mining success
        If ValidateBlock(block):  // Validate the block
            AddBlockToBlockchain(block)  // Submit the block
            RewardMiner(minerID)  // Reward the miner
