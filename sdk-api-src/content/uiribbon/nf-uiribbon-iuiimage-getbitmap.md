---
UID: NF:uiribbon.IUIImage.GetBitmap
title: IUIImage::GetBitmap
author: windows-sdk-content
description: Retrieves a bitmap to display as an icon in the ribbon and context popup UI of the Windows Ribbon framework.
old-location: windowsribbon\windowsribbon_iuiimage_getbitmap.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiimage\getbitmap.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetBitmap, GetBitmap method [Windows Ribbon], GetBitmap method [Windows Ribbon],IUIImage interface, IUIImage interface [Windows Ribbon],GetBitmap method, IUIImage.GetBitmap, IUIImage::GetBitmap, scenicintent_IUIImage_GetBitmap, uiribbon/IUIImage::GetBitmap, windowsribbon.windowsribbon_iuiimage_getbitmap
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
req.lib: 
req.dll: Mshtml.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUIImage.GetBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



<b>IUIImage::GetBitmap</b> is called on image property callback triggered by <a href="https://msdn.microsoft.com/en-us/library/Dd371375(v=VS.85).aspx">InvalidateUICommand</a>. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd371367(v=VS.85).aspx">IUIImage</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371365(v=VS.85).aspx">IUIImageFromBitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371192(v=VS.85).aspx">Windows Ribbon Framework Samples</a>
 

 

