---
UID: NN:uiribbon.IUIImage
title: IUIImage (uiribbon.h)
description: The IUIImage interface is implemented by the application and defines the method for retrieving an image to display in the ribbon and context popup UI of the Windows Ribbon framework .
old-location: windowsribbon\windowsribbon_iuiimage.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiimage\iuiimage.htm
ms.date: 12/05/2018
ms.keywords: IUIImage, IUIImage interface [Windows Ribbon], IUIImage interface [Windows Ribbon],described, scenicintent_IUIImage, uiribbon/IUIImage, windowsribbon.windowsribbon_iuiimage
ms.topic: interface
f1_keywords:
- uiribbon/IUIImage
dev_langs:
- c++
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
req.dll: Uiribbon.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uiribbon.dll
api_name:
- IUIImage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIImage interface


## -description


The <b>IUIImage</b> interface is implemented by the application and defines the method 
		for retrieving an image to display in the ribbon and context popup UI of the Windows Ribbon framework .


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIImage</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIImage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIImage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuiimage-getbitmap">GetBitmap</a>
</td>
<td align="left" width="63%">
Retrieves a bitmap to display as an icon in the ribbon and context popup UI of the Ribbon framework.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap">IUIImageFromBitmap</a>



<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>
 

 

