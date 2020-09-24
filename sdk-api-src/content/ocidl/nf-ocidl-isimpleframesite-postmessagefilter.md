---
UID: NF:ocidl.ISimpleFrameSite.PostMessageFilter
title: ISimpleFrameSite::PostMessageFilter (ocidl.h)
description: Sends the simple frame site a message that is received by a control's own window after the control has processed the message.
helpviewer_keywords: ["ISimpleFrameSite interface [COM]","PostMessageFilter method","ISimpleFrameSite.PostMessageFilter","ISimpleFrameSite::PostMessageFilter","PostMessageFilter","PostMessageFilter method [COM]","PostMessageFilter method [COM]","ISimpleFrameSite interface","_ctrl_isimpleframesite_postmessagefilter","com.isimpleframesite_postmessagefilter","ocidl/ISimpleFrameSite::PostMessageFilter"]
old-location: com\isimpleframesite_postmessagefilter.htm
tech.root: com
ms.assetid: b9725ef9-16e0-4574-9b94-826814a396be
ms.date: 12/05/2018
ms.keywords: ISimpleFrameSite interface [COM],PostMessageFilter method, ISimpleFrameSite.PostMessageFilter, ISimpleFrameSite::PostMessageFilter, PostMessageFilter, PostMessageFilter method [COM], PostMessageFilter method [COM],ISimpleFrameSite interface, _ctrl_isimpleframesite_postmessagefilter, com.isimpleframesite_postmessagefilter, ocidl/ISimpleFrameSite::PostMessageFilter
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - ISimpleFrameSite::PostMessageFilter
 - ocidl/ISimpleFrameSite::PostMessageFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - ISimpleFrameSite.PostMessageFilter
---

# ISimpleFrameSite::PostMessageFilter


## -description

Sends the simple frame site a message that is received by a control's own window after the control has processed the message.

## -parameters

### -param hWnd [in]

A handle of the control window receiving the message.

### -param msg [in]

The message received by the simple frame site.

### -param wp [in]

The <b>WPARAM</b> of the message.

### -param lp [in]

The <b>LPARAM</b> of the message.

### -param plResult [out]

 A pointer to the variable that receives the result of the message processing.

### -param dwCookie [in]

The value that was returned by <a href="/windows/desktop/api/ocidl/nf-ocidl-isimpleframesite-premessagefilter">ISimpleFrameSite::PreMessageFilter</a> through its <i>pdwCookie</i> parameter.

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
The site processed the message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The site did not process the message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The site does not filter any messages.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-isimpleframesite">ISimpleFrameSite</a>