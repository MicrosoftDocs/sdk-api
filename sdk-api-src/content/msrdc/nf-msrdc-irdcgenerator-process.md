---
UID: NF:msrdc.IRdcGenerator.Process
title: IRdcGenerator::Process
author: windows-sdk-content
description: Processes the input data and produces 0 or more output bytes.
old-location: rdc\irdcgenerator_process.htm
old-project: Rdc
ms.assetid: 34d19eee-0fa9-4ac3-a33b-9f01cfa06371
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IRdcGenerator interface [Remote Differential Compression],Process method, IRdcGenerator.Process, IRdcGenerator::Process, Process, Process method [Remote Differential Compression], Process method [Remote Differential Compression],IRdcGenerator interface, fs.irdcgenerator_process, msrdc/IRdcGenerator::Process, rdc.irdcgenerator_process
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsRdc.dll
tech.root: 
req.typenames: RdcMappingAccessMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	IRdcGenerator.Process
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRdcGenerator::Process


## -description


The <b>Process</b> method processes the input 
    data and produces 0 or more output bytes. This method must be called repeatedly until the 
    <b>BOOL</b> pointed to by <i>endOfOutput</i> is set to 
    <b>TRUE</b>.


## -parameters




### -param endOfInput [in]

Set to <b>TRUE</b> when the input buffer pointed to by the 
      <i>inputBuffer</i> parameter contains the remaining input available.


### -param endOfOutput [out]

Address of a <b>BOOL</b> that is set to <b>TRUE</b> when the 
      processing is complete for all data.


### -param inputBuffer [in, out]

Address of an <a href="https://msdn.microsoft.com/1792e40b-c363-4732-9613-301c3e6e4da7">RdcBufferPointer</a> structure that 
      contains the input buffer. On successful return, the <b>m_Used</b> member of this structure 
      will be filled with the number of bytes by this call.


### -param depth [in]

The number of levels of signatures to generate. This must match the number of levels specified when the 
      generator was created.


### -param outputBuffers [out]

The address of an array of <a href="https://msdn.microsoft.com/1792e40b-c363-4732-9613-301c3e6e4da7">RdcBufferPointer</a> structures that 
      will receive the output buffers. The <b>m_Used</b> member of these structures will be filled with the number of bytes returned in the buffer.


### -param rdc_ErrorCode [out]

The address of an <a href="https://msdn.microsoft.com/32e9eab0-dc6e-4e04-af8a-bc2ed4adf0be">RDC_ErrorCode</a> enumeration that is 
      filled with an RDC specific error code if the return value from the 
      <b>Process</b> method is 
      <b>E_FAIL</b>. If this value is <b>RDC_Win32ErrorCode</b>, then the 
      return value of the <b>Process</b> method contains the 
      specific error code.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/0288318a-0974-4870-b423-87c52090eb33">IRdcGenerator</a>



<a href="https://msdn.microsoft.com/32e9eab0-dc6e-4e04-af8a-bc2ed4adf0be">RDC_ErrorCode</a>



<a href="https://msdn.microsoft.com/1792e40b-c363-4732-9613-301c3e6e4da7">RdcBufferPointer</a>
 

 

