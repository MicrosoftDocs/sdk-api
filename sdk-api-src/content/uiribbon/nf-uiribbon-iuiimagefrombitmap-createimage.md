---
UID: NF:uiribbon.IUIImageFromBitmap.CreateImage
title: IUIImageFromBitmap::CreateImage (uiribbon.h)
description: Creates an IUIImage object from a bitmap image.
helpviewer_keywords: ["CreateImage","CreateImage method [Windows Ribbon]","CreateImage method [Windows Ribbon]","IUIImageFromBitmap interface","IUIImageFromBitmap interface [Windows Ribbon]","CreateImage method","IUIImageFromBitmap.CreateImage","IUIImageFromBitmap::CreateImage","scenicintent_IUIImageFromBitmap_CreateImage","uiribbon/IUIImageFromBitmap::CreateImage","windowsribbon.windowsribbon_iuiimagefrombitmap_createimage"]
old-location: windowsribbon\windowsribbon_iuiimagefrombitmap_createimage.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiimagefrombitmap\createimage.htm
ms.date: 12/05/2018
ms.keywords: CreateImage, CreateImage method [Windows Ribbon], CreateImage method [Windows Ribbon],IUIImageFromBitmap interface, IUIImageFromBitmap interface [Windows Ribbon],CreateImage method, IUIImageFromBitmap.CreateImage, IUIImageFromBitmap::CreateImage, scenicintent_IUIImageFromBitmap_CreateImage, uiribbon/IUIImageFromBitmap::CreateImage, windowsribbon.windowsribbon_iuiimagefrombitmap_createimage
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mshtml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
ms.custom: 19H1
f1_keywords:
 - IUIImageFromBitmap::CreateImage
 - uiribbon/IUIImageFromBitmap::CreateImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUIImageFromBitmap.CreateImage
---

# IUIImageFromBitmap::CreateImage


## -description

Creates an <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage">IUIImage</a> object from a bitmap image.

## -parameters

### -param bitmap [in]

Type: <b>HBITMAP</b>

A handle to the bitmap that contains the image.

### -param options [in]

Type: <b><a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_ownership">UI_OWNERSHIP</a></b>

The <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_ownership">ownership conditions</a> under which 
					an image is created.
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>UI_OWNERSHIP_TRANSFER</td>
<td>If <b>UI_OWNERSHIP_TRANSFER</b> is specified as the value of 
				<i>options</i>, then the Ribbon framework owns 
					the handle to the bitmap (HBITMAP) through the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage">IUIImage</a> object and 
					releases it when the framework no longer requires it.
				<div class="alert"><b>Note</b>  This option prevents the Ribbon host application from safely referencing the same HBITMAP 
					elsewhere in the application UI.
				</div>
<div> </div>
</td>
</tr>
<tr>
<td>UI_OWNERSHIP_COPY</td>
<td>If <b>UI_OWNERSHIP_COPY</b> is specified as the value of 
				<i>options</i>, then the host application owns the 
					HBITMAP and is able to reference the same HBITMAP for use elsewhere in the 
					UI.
				<div class="alert"><b>Note</b>  This option places responsibility for releasing the HBITMAP on the 
					host application.
				</div>
<div> </div>
</td>
</tr>
</table>

### -param image [out]

Type: <b><a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage">IUIImage</a>**</b>

When this method returns, contains the address of a pointer variable that receives the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage">IUIImage</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This factory method is useful when an application dynamically generates an image 
				 resource and wants to pass the new HBITMAP to the Ribbon, 
				 for example, loading a Portable Network Graphics (PNG) through the Windows Imaging Component (WIC) or using 
				 <a href="/previous-versions//ms532292(v=vs.85)">CreateDIBSection</a> to create an image for a new style 
				 in a styles gallery.
			

This method is also useful for applications that require a 
				pre-existing bitmap image that has not been rendered obsolete by the Ribbon, 
				for example, a legacy toolbar image strip.
			

Specify <b>UI_OWNERSHIP_COPY</b> as the value for <i>options</i> if the Ribbon is being implemented in an 
				existing application and minimal code changes are required. This method uses extra memory 
				for the additional image.
			

Specify <b>UI_OWNERSHIP_TRANSFER</b> as the value for <i>options</i> to minimize memory usage.

## -see-also

<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap">IUIImageFromBitmap</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>