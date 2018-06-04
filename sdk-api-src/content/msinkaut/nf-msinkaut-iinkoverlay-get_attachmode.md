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

# IInkOverlay::get_AttachMode


## -description



Gets or sets the value that specifies whether the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object is attached behind or in front of the known window.



This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  An error occurs if the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object is not disabled before setting this property. To disable the <b>InkOverlay</b> object, set the <a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a> property to <b>FALSE</b>. You can then set the <b>AttachMode</b> property and re-enable the object by setting the <b>Enabled</b> property to <b>TRUE</b>.</div>
<div> </div>
<div class="alert"><b>Caution</b>  If <b>AttachMode</b> is set to <a href="https://msdn.microsoft.com/5b46c6fc-2415-4ed2-a2f9-47a6e8455ff0">InFront</a> and then a control is added to the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a>'s attached control, then you will have to reset the <b>InkOverlay</b>'s <a href="https://msdn.microsoft.com/1a8b933f-a4f0-46f5-8b41-df89b6378e9f">hWnd</a>. First set <a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a> to <b>FALSE</b>, then set the <b>hWnd</b> property, and then set <b>Enabled</b> to <b>TRUE</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ab55a399-1990-4cfc-a4ab-834a5db8d7a9">Enabled Property</a>



<a href="tablet.iinkoverlay">IInkOverlay</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/5b46c6fc-2415-4ed2-a2f9-47a6e8455ff0">InkOverlayAttachMode Enumeration</a>
 

 

