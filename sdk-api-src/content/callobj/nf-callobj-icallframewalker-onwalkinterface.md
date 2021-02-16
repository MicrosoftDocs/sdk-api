---
UID: NF:callobj.ICallFrameWalker.OnWalkInterface
title: ICallFrameWalker::OnWalkInterface (callobj.h)
description: Walks through a call frame to look for the specified interface in the call frame. The interface can be manipulated or replaced by paying close attention to the reference count.
helpviewer_keywords: ["ICallFrameWalker interface [COM]","OnWalkInterface method","ICallFrameWalker.OnWalkInterface","ICallFrameWalker::OnWalkInterface","OnWalkInterface","OnWalkInterface method [COM]","OnWalkInterface method [COM]","ICallFrameWalker interface","_com_icallframewalker_onwalkinterface","callobj/ICallFrameWalker::OnWalkInterface","com.icallframewalker_onwalkinterface"]
old-location: com\icallframewalker_onwalkinterface.htm
tech.root: com
ms.assetid: e599536f-87a3-4f71-ac0e-21bdafafd029
ms.date: 12/05/2018
ms.keywords: ICallFrameWalker interface [COM],OnWalkInterface method, ICallFrameWalker.OnWalkInterface, ICallFrameWalker::OnWalkInterface, OnWalkInterface, OnWalkInterface method [COM], OnWalkInterface method [COM],ICallFrameWalker interface, _com_icallframewalker_onwalkinterface, callobj/ICallFrameWalker::OnWalkInterface, com.icallframewalker_onwalkinterface
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
 - ICallFrameWalker::OnWalkInterface
 - callobj/ICallFrameWalker::OnWalkInterface
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
 - ICallFrameWalker.OnWalkInterface
---

# ICallFrameWalker::OnWalkInterface


## -description

Walks through a call frame to look for the specified interface in the call frame. The interface can be manipulated or replaced by paying close attention to the reference count.

## -parameters

### -param iid [in]

The IID of the interface to be found.

### -param ppvInterface [in]

A points to the buffer from which the activation record is to be reconstituted.

### -param fIn [in]

This parameter is nonzero if an interface is inside an [in] or [in, out] parameter.

### -param fOut [in]

This parameter is nonzero if an interface is inside an [out] or [in, out] parameter.

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

<a href="/windows/desktop/api/callobj/nn-callobj-icallframewalker">ICallFrameWalker</a>