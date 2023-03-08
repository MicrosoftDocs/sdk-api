---
UID: NF:msinkaut.IInkPicture.put_InkEnabled
title: IInkPicture::put_InkEnabled (msinkaut.h)
description: Gets or sets a value that specifies whether the InkPicture control collects pen input (in-air packets, cursor in range events, and so on). (Put)
helpviewer_keywords: ["3af59de9-0239-47ab-b3b3-1f1baecb169f","IInkPicture interface [Tablet PC]","InkEnabled property","IInkPicture.InkEnabled","IInkPicture.put_InkEnabled","IInkPicture::InkEnabled","IInkPicture::get_InkEnabled","IInkPicture::put_InkEnabled","InkEnabled property [Tablet PC]","InkEnabled property [Tablet PC]","IInkPicture interface","InkPicture.get_InkEnabled","InkPicture.put_InkEnabled","get_InkEnabled","msinkaut/IInkPicture::InkEnabled","msinkaut/IInkPicture::get_InkEnabled","msinkaut/IInkPicture::put_InkEnabled","put_InkEnabled","tablet.inkpicture_inkenabled"]
old-location: tablet\inkpicture_inkenabled.htm
tech.root: tablet
ms.assetid: 3af59de9-0239-47ab-b3b3-1f1baecb169f
ms.date: 12/05/2018
ms.keywords: 3af59de9-0239-47ab-b3b3-1f1baecb169f, IInkPicture interface [Tablet PC],InkEnabled property, IInkPicture.InkEnabled, IInkPicture.put_InkEnabled, IInkPicture::InkEnabled, IInkPicture::get_InkEnabled, IInkPicture::put_InkEnabled, InkEnabled property [Tablet PC], InkEnabled property [Tablet PC],IInkPicture interface, InkPicture.get_InkEnabled, InkPicture.put_InkEnabled, get_InkEnabled, msinkaut/IInkPicture::InkEnabled, msinkaut/IInkPicture::get_InkEnabled, msinkaut/IInkPicture::put_InkEnabled, put_InkEnabled, tablet.inkpicture_inkenabled
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkPicture::put_InkEnabled
 - msinkaut/IInkPicture::put_InkEnabled
dev_langs:
 - c++
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
---

# IInkPicture::put_InkEnabled


## -description

Gets or sets a value that specifies whether the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control collects pen input (in-air packets, cursor in range events, and so on).



This property is read/write.

## -parameters

## -remarks

The <a href="/windows/desktop/tablet/inkpicture-control">InkPicture</a> control collects ink in Windows Vista, Microsoft Windows XP Tablet PC Edition or any edition of Windows 2000, Windows Server 2003, or Windows XP on which the Windows XP Tablet PC Edition Software Development Kit (SDK) is installed. However, handwriting recognition occurs only if Windows Vista, Windows XP Tablet PC Edition, or the Recognizer Pack is installed.

In any edition of Windows 2000, Windows Server 2003, or of Windows XP other than Windows XP Tablet PC Edition, the <b>InkEnabled</b> property is always <b>FALSE</b> if the Tablet PC SDK is not installed.

If the window input rectangle of an enabled object (set in the constructor or with the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle">SetWindowInputRectangle Method</a>) overlaps the window input rectangle of another enabled object, the E_INK_OVERLAPPING_INPUT_RECT error is returned.

<div class="alert"><b>Note</b>  Overlap can occur without an error as long as only one of the input rectangles is enabled at any time.</div>
<div> </div>
While the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control is not enabled, you receive no events.

When the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled">Enabled</a> property of a container <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control is set to <b>VARIANT_FALSE</b>, all of its contained controls are disabled as well.

You cannot set this property to <b>VARIANT_FALSE</b> while the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control is collecting ink (the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink">CollectingInk Property</a> property is <b>VARIANT_TRUE</b>).

For best results, set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled">Enabled</a> property to <b>VARIANT_FALSE</b> when an application shuts down.

This property must be set to <b>VARIANT_FALSE</b> before setting or calling specific properties and methods of the control. If you try to change the specified properties or call the specified methods, an error occurs. The following properties and methods cannot be set or called unless the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled">Enabled</a> property is first set to <b>VARIANT_FALSE</b>:

<ol>
<li>Properties:<ul>
<li>
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink">Ink</a>
</li>
<li>
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx">MarginX Property</a>
</li>
<li>
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy">MarginY Property</a>
</li>
</ul>
</li>
<li>Methods:<ul>
<li>
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode">SetAllTabletsMode Method</a>
</li>
<li>
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode">SetSingleTabletIntegratedMode Method</a>
</li>
</ul>
</li>
</ol>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode">CollectionMode Property [InkPicture Control]</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode">EditingMode Property [InkPicture Control]</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled">Enabled Property [InkPicture Control]</a>



<a href="../msinkaut/nn-msinkaut-iinkpicture.md">IInkPicture</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink">Ink Property [InkPicture Control]</a>



<a href="/windows/desktop/tablet/inkpicture-control">InkPicture Control</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx">MarginX Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy">MarginY Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode">SetAllTabletsMode Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode">SetSingleTabletIntegratedMode Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle">SetWindowInputRectangle Method</a>
