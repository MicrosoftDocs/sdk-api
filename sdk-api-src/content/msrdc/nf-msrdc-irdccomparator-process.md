---
UID: NF:msrdc.IRdcComparator.Process
title: IRdcComparator::Process
author: windows-sdk-content
description: Compares two signature streams (seed and source) and produces a needs list, which describes the chunks of file data needed to create the target file.
old-location: rdc\irdccomparator_process.htm
old-project: Rdc
ms.assetid: cc98a90c-ba82-4b92-a56c-07496a843089
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IRdcComparator interface [Remote Differential Compression],Process method, IRdcComparator.Process, IRdcComparator::Process, Process, Process method [Remote Differential Compression], Process method [Remote Differential Compression],IRdcComparator interface, fs.irdccomparator_process, msrdc/IRdcComparator::Process, rdc.irdccomparator_process
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.redist: 
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
req.type-library: 
tech.root: 
req.typenames: RdcMappingAccessMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcComparator.Process
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRdcComparator::Process


## -description


The <b>Process</b> method 
    compares two signature streams (seed and source) and produces a needs list, which describes the chunks of file data needed to create 
    the target file. The seed signature file may be read multiple times, depending on the size of the 
    source signature file.


## -parameters




### -param endOfInput [in]

Set to <b>TRUE</b> if the <i>inputBuffer</i> parameter contains all 
      remaining input.


### -param endOfOutput [out]

Address of a <b>BOOL</b> that on successful completion is set to 
      <b>TRUE</b> if all output data has been generated.


### -param inputBuffer [in, out]

Address of a <a href="https://msdn.microsoft.com/1792e40b-c363-4732-9613-301c3e6e4da7">RdcBufferPointer</a> structure containing 
      information about the input buffer. The <b>m_Used</b> member of this structure is used to 
      indicate how much input, if any, was processed during this call.


### -param outputBuffer [in, out]

Address of a <a href="https://msdn.microsoft.com/92a1fae7-5ada-4f7d-a736-c93bc404a418">RdcNeedPointer</a> structure containing 
      information about the output buffer. On input the <b>m_Size</b> member of this structure 
      must contain the number of <a href="https://msdn.microsoft.com/086e82f1-b033-48e2-b648-895c04751cc9">RdcNeed</a> structures in the array 
      pointed to by the <b>m_Data</b> member, and the <b>m_Used</b> member 
      must be zero. On output the <b>m_Used</b> member will contain the number of 
      <b>RdcNeed</b> structures in the array pointed to by the 
      <b>m_Data</b> member.


### -param rdc_ErrorCode [out]

The address of a <a href="https://msdn.microsoft.com/32e9eab0-dc6e-4e04-af8a-bc2ed4adf0be">RDC_ErrorCode</a> enumeration that is 
      filled with an RDC specific error code if the return value from the 
      <b>Process</b> method is 
      <b>E_FAIL</b>. If this value is <b>RDC_Win32ErrorCode</b>, then the 
      return value of the <b>Process</b> method contains the 
      specific error code.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



On successful return, iterate through each <a href="https://msdn.microsoft.com/086e82f1-b033-48e2-b648-895c04751cc9">RdcNeed</a> structure 
   returned in the array pointed to by the <b>m_Data</b> member of the 
   <i>outputBuffer</i> parameter, and copy the specified chunk of the source or seed data to the 
   target data.




## -see-also




<a href="https://msdn.microsoft.com/ad39b922-3271-491e-b74b-80a1f647e663">IRdcComparator</a>



<a href="https://msdn.microsoft.com/32e9eab0-dc6e-4e04-af8a-bc2ed4adf0be">RDC_ErrorCode</a>



<a href="https://msdn.microsoft.com/1792e40b-c363-4732-9613-301c3e6e4da7">RdcBufferPointer</a>



<a href="https://msdn.microsoft.com/92a1fae7-5ada-4f7d-a736-c93bc404a418">RdcNeedPointer</a>
 

 

