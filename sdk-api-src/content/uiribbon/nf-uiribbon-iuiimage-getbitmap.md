---
UID: NF:uiribbon.IUIImage.GetBitmap
title: IUIImage::GetBitmap
author: windows-driver-content
description: Retrieves a bitmap to display as an icon in the ribbon and context popup UI of the Windows Ribbon framework.
old-location: windowsribbon\windowsribbon_iuiimage_getbitmap.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiimage\getbitmap.htm
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetBitmap, GetBitmap method [Windows Ribbon], GetBitmap method [Windows Ribbon],IUIImage interface, IUIImage interface [Windows Ribbon],GetBitmap method, IUIImage.GetBitmap, IUIImage::GetBitmap, scenicintent_IUIImage_GetBitmap, uiribbon/IUIImage::GetBitmap, windowsribbon.windowsribbon_iuiimage_getbitmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: UI_VIEWVERB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mshtml.dll
api_name:
-	IUIImage.GetBitmap
product: Windows
targetos: Windows
req.lib: 
req.dll: Mshtml.dll
req.irql: 
req.product: Windows UI
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IUIImage::GetBitmap</b> is called on image property callback triggered by <a href="https://msdn.microsoft.com/6f6f6815-5523-42d9-a6b2-a21dd26756c0">InvalidateUICommand</a>. 




## -see-also




<a href="https://msdn.microsoft.com/27c76385-82ff-485d-b653-a384765b0be8">IUIImage</a>



<a href="https://msdn.microsoft.com/f2b98d96-895e-40aa-9969-98bf1c0c8e5f">IUIImageFromBitmap</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 

