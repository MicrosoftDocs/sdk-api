---
UID: NF:msinkaut.IInkOverlay.get_AttachMode
title: IInkOverlay::get_AttachMode (msinkaut.h)
author: windows-sdk-content
description: Gets or sets the value that specifies whether the InkOverlay object is attached behind or in front of the known window.
old-location: tablet\inkoverlay_attachmode.htm
tech.root: tablet
ms.assetid: 638da0e4-10cc-47e7-91ad-807be3ff8c2d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 638da0e4-10cc-47e7-91ad-807be3ff8c2d, AttachMode property [Tablet PC], AttachMode property [Tablet PC],IInkOverlay interface, Behind, IInkOverlay interface [Tablet PC],AttachMode property, IInkOverlay.AttachMode, IInkOverlay.get_AttachMode, IInkOverlay::AttachMode, IInkOverlay::get_AttachMode, IInkOverlay::put_AttachMode, InFront, InkOverlay.get_AttachMode, InkOverlay.put_AttachMode, get_AttachMode, msinkaut/IInkOverlay::AttachMode, msinkaut/IInkOverlay::get_AttachMode, msinkaut/IInkOverlay::put_AttachMode, put_AttachMode, tablet.inkoverlay_attachmode
ms.topic: method
f1_keywords: 
 - "msinkaut/IInkOverlay.AttachMode"
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkOverlay.AttachMode
 - IInkOverlay.get_AttachMode
 - IInkOverlay.put_AttachMode
 - InkOverlay.get_AttachMode
 - InkOverlay.put_AttachMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkOverlay::get_AttachMode


## -description



Gets or sets the value that specifies whether the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object is attached behind or in front of the known window.



This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  An error occurs if the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object is not disabled before setting this property. To disable the <b>InkOverlay</b> object, set the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled</a> property to <b>FALSE</b>. You can then set the <b>AttachMode</b> property and re-enable the object by setting the <b>Enabled</b> property to <b>TRUE</b>.</div>
<div> </div>
<div class="alert"><b>Caution</b>  If <b>AttachMode</b> is set to <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayattachmode">InFront</a> and then a control is added to the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>'s attached control, then you will have to reset the <b>InkOverlay</b>'s <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd">hWnd</a>. First set <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled</a> to <b>FALSE</b>, then set the <b>hWnd</b> property, and then set <b>Enabled</b> to <b>TRUE</b>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled Property</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846799(v=VS.85).aspx">IInkOverlay</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayattachmode">InkOverlayAttachMode Enumeration</a>
 

 

