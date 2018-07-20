---
UID: NF:msinkaut.IInkPicture.put_InkEnabled
title: IInkPicture::put_InkEnabled
author: windows-sdk-content
description: Gets or sets a value that specifies whether the InkPicture control collects pen input (in-air packets, cursor in range events, and so on).
old-location: tablet\inkpicture_inkenabled.htm
old-project: tablet
ms.assetid: 3af59de9-0239-47ab-b3b3-1f1baecb169f
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: 3af59de9-0239-47ab-b3b3-1f1baecb169f, IInkPicture interface [Tablet PC],InkEnabled property, IInkPicture.InkEnabled, IInkPicture.put_InkEnabled, IInkPicture::InkEnabled, IInkPicture::get_InkEnabled, IInkPicture::put_InkEnabled, InkEnabled property [Tablet PC], InkEnabled property [Tablet PC],IInkPicture interface, InkPicture.get_InkEnabled, InkPicture.put_InkEnabled, get_InkEnabled, msinkaut/IInkPicture::InkEnabled, msinkaut/IInkPicture::get_InkEnabled, msinkaut/IInkPicture::put_InkEnabled, put_InkEnabled, tablet.inkpicture_inkenabled
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkPicture.InkEnabled
 - IInkPicture.get_InkEnabled
 - IInkPicture.put_InkEnabled
 - InkPicture.get_InkEnabled
 - InkPicture.put_InkEnabled
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkPicture::put_InkEnabled


## -description



Gets or sets a value that specifies whether the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control collects pen input (in-air packets, cursor in range events, and so on).



This property is read/write.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/1ced9779-dae5-4f9a-8a68-b2c0d041d5b4">InkPicture</a> control collects ink in Windows Vista, Microsoft Windows XP Tablet PC Edition or any edition of Windows 2000, Windows Server 2003, or Windows XP on which the Windows XP Tablet PC Edition Software Development Kit (SDK) is installed. However, handwriting recognition occurs only if Windows Vista, Windows XP Tablet PC Edition, or the Recognizer Pack is installed.

In any edition of Windows 2000, Windows Server 2003, or of Windows XP other than Windows XP Tablet PC Edition, the <b>InkEnabled</b> property is always <b>FALSE</b> if the Tablet PC SDK is not installed.

If the window input rectangle of an enabled object (set in the constructor or with the <a href="https://msdn.microsoft.com/3602a550-d37b-4a78-b949-04f5e3cb923a">SetWindowInputRectangle Method</a>) overlaps the window input rectangle of another enabled object, the E_INK_OVERLAPPING_INPUT_RECT error is returned.

<div class="alert"><b>Note</b>  Overlap can occur without an error as long as only one of the input rectangles is enabled at any time.</div>
<div> </div>
While the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control is not enabled, you receive no events.

When the <a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a> property of a container <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control is set to <b>VARIANT_FALSE</b>, all of its contained controls are disabled as well.

You cannot set this property to <b>VARIANT_FALSE</b> while the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control is collecting ink (the <a href="https://msdn.microsoft.com/19fbe26e-02a4-4d05-a2e8-25d2f8ae1146">CollectingInk Property</a> property is <b>VARIANT_TRUE</b>).

For best results, set the <a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a> property to <b>VARIANT_FALSE</b> when an application shuts down.

This property must be set to <b>VARIANT_FALSE</b> before setting or calling specific properties and methods of the control. If you try to change the specified properties or call the specified methods, an error occurs. The following properties and methods cannot be set or called unless the <a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a> property is first set to <b>VARIANT_FALSE</b>:

<ol>
<li>Properties:<ul>
<li>
<a href="https://msdn.microsoft.com/8a6001bb-cfb9-4c24-8f99-3c8f0acd443c">Ink</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c463debc-341b-4491-8543-70623bf717d0">MarginX Property</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f5320061-36c7-4dcb-b5d3-3df41ddcac2a">MarginY Property</a>
</li>
</ul>
</li>
<li>Methods:<ul>
<li>
<a href="https://msdn.microsoft.com/30e8c0d3-6cae-476b-8fc5-f0d97b4b16f4">SetAllTabletsMode Method</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b611a078-b38e-4f9b-834f-9a2aa9684931">SetSingleTabletIntegratedMode Method</a>
</li>
</ul>
</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/fe3d1158-b99b-4ae1-a509-c6f34b42615f">CollectionMode Property [InkPicture Control]</a>



<a href="https://msdn.microsoft.com/5767f768-d59c-404e-9098-ab5e0c427c7d">EditingMode Property [InkPicture Control]</a>



<a href="https://msdn.microsoft.com/1c6e9fb4-be51-4d68-8241-17119deeba3f">Enabled Property [InkPicture Control]</a>



<a href="tablet.iinkpicture">IInkPicture</a>



<a href="https://msdn.microsoft.com/8a6001bb-cfb9-4c24-8f99-3c8f0acd443c">Ink Property [InkPicture Control]</a>



<a href="https://msdn.microsoft.com/1ced9779-dae5-4f9a-8a68-b2c0d041d5b4">InkPicture Control</a>



<a href="https://msdn.microsoft.com/c463debc-341b-4491-8543-70623bf717d0">MarginX Property</a>



<a href="https://msdn.microsoft.com/f5320061-36c7-4dcb-b5d3-3df41ddcac2a">MarginY Property</a>



<a href="https://msdn.microsoft.com/30e8c0d3-6cae-476b-8fc5-f0d97b4b16f4">SetAllTabletsMode Method</a>



<a href="https://msdn.microsoft.com/b611a078-b38e-4f9b-834f-9a2aa9684931">SetSingleTabletIntegratedMode Method</a>



<a href="https://msdn.microsoft.com/3602a550-d37b-4a78-b949-04f5e3cb923a">SetWindowInputRectangle Method</a>
 

 

