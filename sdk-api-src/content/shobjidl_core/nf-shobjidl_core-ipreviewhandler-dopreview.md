---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IPreviewHandler::DoPreview


## -description


Directs the preview handler to load data from the source specified in an earlier Initialize method call, and to begin rendering to the previewer window.


## -parameters






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



If the previewer window has not yet been created, then it must be created after this method has been called. The preview handler is responsible for painting the area specified in <a href="https://msdn.microsoft.com/a323811a-8244-40a0-a6b2-68572639be5f">IPreviewHandler::SetWindow</a> or <a href="https://msdn.microsoft.com/03353962-6905-4b13-bf7a-f1767767a7df">IPreviewHandler::SetRect</a>.  If these methods are called while the preview handler is rendering, the window must be reparented/resized without stopping or restarting the rendering of the item.

This method should be called only after <a href="https://msdn.microsoft.com/a323811a-8244-40a0-a6b2-68572639be5f">IPreviewHandler::SetWindow</a> has been called.


              Aditionally, this method should be called only after <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>, or <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> has been called.
            

<div class="alert"><b>Note</b>  Do not actually create the previewer window until this method has been called.</div>
<div> </div>


