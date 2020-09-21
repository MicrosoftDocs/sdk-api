---
UID: NF:callobj.ICallFrame.FreeParam
title: ICallFrame::FreeParam (callobj.h)
description: Frees the specified parameter in the frame.
helpviewer_keywords: ["FreeParam","FreeParam method [COM]","FreeParam method [COM]","ICallFrame interface","ICallFrame interface [COM]","FreeParam method","ICallFrame.FreeParam","ICallFrame::FreeParam","_com_icallframe_freeparam","callobj/ICallFrame::FreeParam","com.icallframe_freeparam"]
old-location: com\icallframe_freeparam.htm
tech.root: com
ms.assetid: b141bfc4-de1b-4251-b88f-551d0805e9b6
ms.date: 12/05/2018
ms.keywords: FreeParam, FreeParam method [COM], FreeParam method [COM],ICallFrame interface, ICallFrame interface [COM],FreeParam method, ICallFrame.FreeParam, ICallFrame::FreeParam, _com_icallframe_freeparam, callobj/ICallFrame::FreeParam, com.icallframe_freeparam
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
 - ICallFrame::FreeParam
 - callobj/ICallFrame::FreeParam
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
 - ICallFrame.FreeParam
---

# ICallFrame::FreeParam


## -description

Frees the specified parameter in the frame.

## -parameters

### -param iparam [in]

The number of the parameter to be freed.

### -param freeFlags [in]

Represents flags from the <a href="/windows/desktop/api/callobj/ne-callobj-callframe_free">CALLFRAME_FREE</a> enumeration.

### -param pWalkerFree [in]

A pointer to an instance of the <a href="/windows/desktop/api/callobj/nn-callobj-icallframewalker">ICallFrameWalker</a> interface. When specified, a callback is made for each interface pointer encountered while freeing occurs. If this parameter is not specified, then the interface pointers are freed by the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method.

### -param nullFlags [in]

Represents flags from the <a href="/windows/desktop/api/callobj/ne-callobj-callframe_null">CALLFRAME_NULL</a> enumeration.

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

<a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>