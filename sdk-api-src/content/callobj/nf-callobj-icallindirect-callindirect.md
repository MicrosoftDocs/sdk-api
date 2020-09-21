---
UID: NF:callobj.ICallIndirect.CallIndirect
title: ICallIndirect::CallIndirect (callobj.h)
description: Invokes one of the methods in the interface with an indirect reference to the arguments of the invocation.
helpviewer_keywords: ["CallIndirect","CallIndirect method [COM]","CallIndirect method [COM]","ICallIndirect interface","ICallIndirect interface [COM]","CallIndirect method","ICallIndirect.CallIndirect","ICallIndirect::CallIndirect","_com_icallindirect_callindirect","callobj/ICallIndirect::CallIndirect","com.icallindirect_callindirect"]
old-location: com\icallindirect_callindirect.htm
tech.root: com
ms.assetid: d017ad36-8779-4107-8ee3-f44589f9e802
ms.date: 12/05/2018
ms.keywords: CallIndirect, CallIndirect method [COM], CallIndirect method [COM],ICallIndirect interface, ICallIndirect interface [COM],CallIndirect method, ICallIndirect.CallIndirect, ICallIndirect::CallIndirect, _com_icallindirect_callindirect, callobj/ICallIndirect::CallIndirect, com.icallindirect_callindirect
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICallIndirect::CallIndirect
 - callobj/ICallIndirect::CallIndirect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallIndirect.CallIndirect
---

# ICallIndirect::CallIndirect


## -description

Invokes one of the methods in the interface with an indirect reference to the arguments of the invocation.

## -parameters

### -param phrReturn [out]

The value returned from the invocation of the method.

### -param iMethod [in]

The method number to be invoked.

### -param pvArgs [in]

A pointer to the stack frame with which to make the invocation. Details of the exact representation of this stack frame are processor-architecture specific.

### -param cbArgs [out]

The number of bytes to be popped from the stack to clear the stack of arguments to this invocation.

## -returns

This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/callobj/nn-callobj-icallindirect">ICallIndirect</a>