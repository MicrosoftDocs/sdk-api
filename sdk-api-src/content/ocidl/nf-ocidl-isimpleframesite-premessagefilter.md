---
UID: NF:ocidl.ISimpleFrameSite.PreMessageFilter
title: ISimpleFrameSite::PreMessageFilter (ocidl.h)
description: Provides a site with the opportunity to process a message that is received by a control's own window before the control itself does any processing.
helpviewer_keywords: ["ISimpleFrameSite interface [COM]","PreMessageFilter method","ISimpleFrameSite.PreMessageFilter","ISimpleFrameSite::PreMessageFilter","PreMessageFilter","PreMessageFilter method [COM]","PreMessageFilter method [COM]","ISimpleFrameSite interface","_ctrl_isimpleframesite_premessagefilter","com.isimpleframesite_premessagefilter","ocidl/ISimpleFrameSite::PreMessageFilter"]
old-location: com\isimpleframesite_premessagefilter.htm
tech.root: com
ms.assetid: f308ea77-12e7-450b-8b0f-252f1d240388
ms.date: 12/05/2018
ms.keywords: ISimpleFrameSite interface [COM],PreMessageFilter method, ISimpleFrameSite.PreMessageFilter, ISimpleFrameSite::PreMessageFilter, PreMessageFilter, PreMessageFilter method [COM], PreMessageFilter method [COM],ISimpleFrameSite interface, _ctrl_isimpleframesite_premessagefilter, com.isimpleframesite_premessagefilter, ocidl/ISimpleFrameSite::PreMessageFilter
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
 - ISimpleFrameSite::PreMessageFilter
 - ocidl/ISimpleFrameSite::PreMessageFilter
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
 - ISimpleFrameSite.PreMessageFilter
---

# ISimpleFrameSite::PreMessageFilter


## -description

Provides a site with the opportunity to process a message that is received by a control's own window before the control itself does any processing.

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

### -param pdwCookie [out]

A pointer to the variable that will be passed to <a href="/windows/desktop/api/ocidl/nf-ocidl-isimpleframesite-postmessagefilter">ISimpleFrameSite::PostMessageFilter</a> if it is called later. This parameter should only contain allocated data if this method returns S_OK so it will also receive a call to <b>PostMessageFilter</b> which can free the allocation. The caller is not in any way responsible for anything returned in this parameter.

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
The simple frame site will not use the message in this filter so more processing can take place.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The site has processed the message and no further processing should occur.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The site does not do any message filtering, indicating that PostMessageFilter need not be called later.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>plResult</i> or <i>pdwCookie</i> is not valid.

</td>
</tr>
</table>

## -remarks

Successful return values indicate whether the site wishes to allow further processing. S_OK indicates further processing, whereas S_FALSE means do not process further. S_OK also indicates that the control must later call <a href="/windows/desktop/api/ocidl/nf-ocidl-isimpleframesite-postmessagefilter">PostMessageFilter</a>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-isimpleframesite">ISimpleFrameSite</a>