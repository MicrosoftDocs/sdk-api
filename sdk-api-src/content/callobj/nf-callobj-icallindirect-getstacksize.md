---
UID: NF:callobj.ICallIndirect.GetStackSize
title: ICallIndirect::GetStackSize (callobj.h)
description: Retrieves the number of bytes that should be popped from the stack in order to return from an invocation of the method.
helpviewer_keywords: ["GetStackSize","GetStackSize method [COM]","GetStackSize method [COM]","ICallIndirect interface","ICallIndirect interface [COM]","GetStackSize method","ICallIndirect.GetStackSize","ICallIndirect::GetStackSize","_com_icallindirect_getstacksize","callobj/ICallIndirect::GetStackSize","com.icallindirect_getstacksize"]
old-location: com\icallindirect_getstacksize.htm
tech.root: com
ms.assetid: 3251c9b1-e076-4bc3-a995-1b0d275929a0
ms.date: 12/05/2018
ms.keywords: GetStackSize, GetStackSize method [COM], GetStackSize method [COM],ICallIndirect interface, ICallIndirect interface [COM],GetStackSize method, ICallIndirect.GetStackSize, ICallIndirect::GetStackSize, _com_icallindirect_getstacksize, callobj/ICallIndirect::GetStackSize, com.icallindirect_getstacksize
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
 - ICallIndirect::GetStackSize
 - callobj/ICallIndirect::GetStackSize
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
 - ICallIndirect.GetStackSize
---

# ICallIndirect::GetStackSize


## -description

Retrieves the number of bytes that should be popped from the stack in order to return from an invocation of the method.

## -parameters

### -param iMethod [in]

The method number.

### -param cbArgs [out]

The number of bytes to be popped from the stack to clear the stack of arguments to an invocation.

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