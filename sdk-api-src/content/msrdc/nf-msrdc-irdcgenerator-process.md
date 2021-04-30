---
UID: NF:msrdc.IRdcGenerator.Process
title: IRdcGenerator::Process (msrdc.h)
description: Processes the input data and produces 0 or more output bytes.
helpviewer_keywords: ["IRdcGenerator interface [Remote Differential Compression]","Process method","IRdcGenerator.Process","IRdcGenerator::Process","Process","Process method [Remote Differential Compression]","Process method [Remote Differential Compression]","IRdcGenerator interface","fs.irdcgenerator_process","msrdc/IRdcGenerator::Process","rdc.irdcgenerator_process"]
old-location: rdc\irdcgenerator_process.htm
tech.root: rdc
ms.assetid: 34d19eee-0fa9-4ac3-a33b-9f01cfa06371
ms.date: 12/05/2018
ms.keywords: IRdcGenerator interface [Remote Differential Compression],Process method, IRdcGenerator.Process, IRdcGenerator::Process, Process, Process method [Remote Differential Compression], Process method [Remote Differential Compression],IRdcGenerator interface, fs.irdcgenerator_process, msrdc/IRdcGenerator::Process, rdc.irdcgenerator_process
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
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRdcGenerator::Process
 - msrdc/IRdcGenerator::Process
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
 - IRdcGenerator.Process
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

Address of an <a href="/windows/win32/api/msrdc/ns-msrdc-rdcbufferpointer">RdcBufferPointer</a> structure that 
      contains the input buffer. On successful return, the <b>m_Used</b> member of this structure 
      will be filled with the number of bytes by this call.

### -param depth [in]

The number of levels of signatures to generate. This must match the number of levels specified when the 
      generator was created.

### -param outputBuffers [out]

The address of an array of <a href="/windows/win32/api/msrdc/ns-msrdc-rdcbufferpointer">RdcBufferPointer</a> structures that 
      will receive the output buffers. The <b>m_Used</b> member of these structures will be filled with the number of bytes returned in the buffer.

### -param rdc_ErrorCode [out]

The address of an <a href="/windows/win32/api/msrdc/ne-msrdc-rdc_errorcode">RDC_ErrorCode</a> enumeration that is 
      filled with an RDC specific error code if the return value from the 
      <b>Process</b> method is 
      <b>E_FAIL</b>. If this value is <b>RDC_Win32ErrorCode</b>, then the 
      return value of the <b>Process</b> method contains the 
      specific error code.

## -returns

This method can return one of these values.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgenerator">IRdcGenerator</a>



<a href="/windows/win32/api/msrdc/ne-msrdc-rdc_errorcode">RDC_ErrorCode</a>



<a href="/windows/win32/api/msrdc/ns-msrdc-rdcbufferpointer">RdcBufferPointer</a>