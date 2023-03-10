---
UID: NF:msrdc.IRdcComparator.Process
title: IRdcComparator::Process (msrdc.h)
description: Compares two signature streams (seed and source) and produces a needs list, which describes the chunks of file data needed to create the target file.
helpviewer_keywords: ["IRdcComparator interface [Remote Differential Compression]","Process method","IRdcComparator.Process","IRdcComparator::Process","Process","Process method [Remote Differential Compression]","Process method [Remote Differential Compression]","IRdcComparator interface","fs.irdccomparator_process","msrdc/IRdcComparator::Process","rdc.irdccomparator_process"]
old-location: rdc\irdccomparator_process.htm
tech.root: rdc
ms.assetid: cc98a90c-ba82-4b92-a56c-07496a843089
ms.date: 12/05/2018
ms.keywords: IRdcComparator interface [Remote Differential Compression],Process method, IRdcComparator.Process, IRdcComparator::Process, Process, Process method [Remote Differential Compression], Process method [Remote Differential Compression],IRdcComparator interface, fs.irdccomparator_process, msrdc/IRdcComparator::Process, rdc.irdccomparator_process
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
req.type-library: 
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRdcComparator::Process
 - msrdc/IRdcComparator::Process
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcComparator.Process
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

Address of a <a href="/windows/win32/api/msrdc/ns-msrdc-rdcbufferpointer">RdcBufferPointer</a> structure containing 
      information about the input buffer. The <b>m_Used</b> member of this structure is used to 
      indicate how much input, if any, was processed during this call.

### -param outputBuffer [in, out]

Address of a <a href="/windows/win32/api/msrdc/ns-msrdc-rdcneedpointer">RdcNeedPointer</a> structure containing 
      information about the output buffer. On input the <b>m_Size</b> member of this structure 
      must contain the number of <a href="/windows/win32/api/msrdc/ns-msrdc-rdcneed">RdcNeed</a> structures in the array 
      pointed to by the <b>m_Data</b> member, and the <b>m_Used</b> member 
      must be zero. On output the <b>m_Used</b> member will contain the number of 
      <b>RdcNeed</b> structures in the array pointed to by the 
      <b>m_Data</b> member.

### -param rdc_ErrorCode [out]

The address of a <a href="/windows/win32/api/msrdc/ne-msrdc-rdc_errorcode">RDC_ErrorCode</a> enumeration that is 
      filled with an RDC specific error code if the return value from the 
      <b>Process</b> method is 
      <b>E_FAIL</b>. If this value is <b>RDC_Win32ErrorCode</b>, then the 
      return value of the <b>Process</b> method contains the 
      specific error code.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

On successful return, iterate through each <a href="/windows/win32/api/msrdc/ns-msrdc-rdcneed">RdcNeed</a> structure 
   returned in the array pointed to by the <b>m_Data</b> member of the 
   <i>outputBuffer</i> parameter, and copy the specified chunk of the source or seed data to the 
   target data.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdccomparator">IRdcComparator</a>



<a href="/windows/win32/api/msrdc/ne-msrdc-rdc_errorcode">RDC_ErrorCode</a>



<a href="/windows/win32/api/msrdc/ns-msrdc-rdcbufferpointer">RdcBufferPointer</a>



<a href="/windows/win32/api/msrdc/ns-msrdc-rdcneedpointer">RdcNeedPointer</a>