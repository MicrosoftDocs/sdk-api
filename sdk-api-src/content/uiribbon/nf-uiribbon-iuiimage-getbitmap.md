---
UID: NF:uiribbon.IUIImage.GetBitmap
title: IUIImage::GetBitmap (uiribbon.h)
description: Retrieves a bitmap to display as an icon in the ribbon and context popup UI of the Windows Ribbon framework.
helpviewer_keywords: ["GetBitmap","GetBitmap method [Windows Ribbon]","GetBitmap method [Windows Ribbon]","IUIImage interface","IUIImage interface [Windows Ribbon]","GetBitmap method","IUIImage.GetBitmap","IUIImage::GetBitmap","scenicintent_IUIImage_GetBitmap","uiribbon/IUIImage::GetBitmap","windowsribbon.windowsribbon_iuiimage_getbitmap"]
old-location: windowsribbon\windowsribbon_iuiimage_getbitmap.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiimage\getbitmap.htm
ms.date: 12/05/2018
ms.keywords: GetBitmap, GetBitmap method [Windows Ribbon], GetBitmap method [Windows Ribbon],IUIImage interface, IUIImage interface [Windows Ribbon],GetBitmap method, IUIImage.GetBitmap, IUIImage::GetBitmap, scenicintent_IUIImage_GetBitmap, uiribbon/IUIImage::GetBitmap, windowsribbon.windowsribbon_iuiimage_getbitmap
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
 - IUIImage::GetBitmap
 - uiribbon/IUIImage::GetBitmap
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
 - IUIImage.GetBitmap
---

# IUIImage::GetBitmap


## -description

Retrieves a bitmap to display as an icon in the ribbon and context popup UI of the Windows Ribbon framework.

## -parameters

### -param bitmap [out]

Type: <b>HBITMAP*</b>

When this method returns, contains a pointer to the handle to the requested bitmap.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IUIImage::GetBitmap</b> is called on image property callback triggered by <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand">InvalidateUICommand</a>.

## -see-also

<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage">IUIImage</a>



<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap">IUIImageFromBitmap</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>