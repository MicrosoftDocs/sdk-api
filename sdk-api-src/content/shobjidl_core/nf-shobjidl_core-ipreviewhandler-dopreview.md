---
UID: NF:shobjidl_core.IPreviewHandler.DoPreview
title: IPreviewHandler::DoPreview (shobjidl_core.h)
description: Directs the preview handler to load data from the source specified in an earlier Initialize method call, and to begin rendering to the previewer window.
helpviewer_keywords: ["DoPreview","DoPreview method [Windows Shell]","DoPreview method [Windows Shell]","IPreviewHandler interface","IPreviewHandler interface [Windows Shell]","DoPreview method","IPreviewHandler.DoPreview","IPreviewHandler::DoPreview","_shell_IPreviewHandler_DoPreview","shell.IPreviewHandler_DoPreview","shobjidl_core/IPreviewHandler::DoPreview"]
old-location: shell\IPreviewHandler_DoPreview.htm
tech.root: shell
ms.assetid: f6bad84f-9089-4905-ad4d-9b69ff9d11d6
ms.date: 12/05/2018
ms.keywords: DoPreview, DoPreview method [Windows Shell], DoPreview method [Windows Shell],IPreviewHandler interface, IPreviewHandler interface [Windows Shell],DoPreview method, IPreviewHandler.DoPreview, IPreviewHandler::DoPreview, _shell_IPreviewHandler_DoPreview, shell.IPreviewHandler_DoPreview, shobjidl_core/IPreviewHandler::DoPreview
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Search 4 or later
ms.custom: 19H1
f1_keywords:
 - IPreviewHandler::DoPreview
 - shobjidl_core/IPreviewHandler::DoPreview
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IPreviewHandler.DoPreview
---

# IPreviewHandler::DoPreview


## -description

Directs the preview handler to load data from the source specified in an earlier Initialize method call, and to begin rendering to the previewer window.



## -returns

Type: <b>HRESULT</b>

This method can return one of these values.

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
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PREVIEWHANDLER_DRM_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Blocked by digital rights management.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PREVIEWHANDLER_NOAUTH</b></dt>
</dl>
</td>
<td width="60%">
Blocked by file permissions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PREVIEWHANDLER_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Item was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PREVIEWHANDLER_CORRUPT</b></dt>
</dl>
</td>
<td width="60%">
Item was corrupt.

</td>
</tr>
</table>

## -remarks

If the previewer window has not yet been created, then it must be created after this method has been called. The preview handler is responsible for painting the area specified in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow">IPreviewHandler::SetWindow</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect">IPreviewHandler::SetRect</a>.  If these methods are called while the preview handler is rendering, the window must be reparented/resized without stopping or restarting the rendering of the item.

This method should be called only after <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow">IPreviewHandler::SetWindow</a> has been called.

Additionally, this method should be called only after <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize">IInitializeWithItem::Initialize</a>, <a href="/windows/desktop/api/propsys/nf-propsys-iinitializewithstream-initialize">IInitializeWithStream::Initialize</a>, or <a href="/windows/desktop/api/propsys/nf-propsys-iinitializewithfile-initialize">IInitializeWithFile::Initialize</a> has been called.
            

<div class="alert"><b>Note</b>  Do not actually create the previewer window until this method has been called.</div>
<div> </div>
