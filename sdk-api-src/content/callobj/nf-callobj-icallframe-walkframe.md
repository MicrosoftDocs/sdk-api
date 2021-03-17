---
UID: NF:callobj.ICallFrame.WalkFrame
title: ICallFrame::WalkFrame (callobj.h)
description: Searches for interface pointers that are reachable from [in], [in, out], or [out] parameters of the frame.
helpviewer_keywords: ["ICallFrame interface [COM]","WalkFrame method","ICallFrame.WalkFrame","ICallFrame::WalkFrame","WalkFrame","WalkFrame method [COM]","WalkFrame method [COM]","ICallFrame interface","_com_icallframe_walkframe","callobj/ICallFrame::WalkFrame","com.icallframe_walkframe"]
old-location: com\icallframe_walkframe.htm
tech.root: com
ms.assetid: 64e4967b-6b54-4416-ae10-04987f13d39a
ms.date: 12/05/2018
ms.keywords: ICallFrame interface [COM],WalkFrame method, ICallFrame.WalkFrame, ICallFrame::WalkFrame, WalkFrame, WalkFrame method [COM], WalkFrame method [COM],ICallFrame interface, _com_icallframe_walkframe, callobj/ICallFrame::WalkFrame, com.icallframe_walkframe
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
 - ICallFrame::WalkFrame
 - callobj/ICallFrame::WalkFrame
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
 - ICallFrame.WalkFrame
---

# ICallFrame::WalkFrame


## -description

Searches for interface pointers that are reachable from [in], [in, out], or [out] parameters of the frame.

## -parameters

### -param walkWhat [in]

Flags from the <a href="/windows/desktop/api/callobj/ne-callobj-callframe_walk">CALLFRAME_WALK</a> enumeration.

### -param pWalker [in]

A pointer to an instance of the <a href="/windows/desktop/api/callobj/nn-callobj-icallframewalker">ICallFrameWalker</a> interface. When specified, a call back is made for each interface pointer encountered. This parameter is optional.

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