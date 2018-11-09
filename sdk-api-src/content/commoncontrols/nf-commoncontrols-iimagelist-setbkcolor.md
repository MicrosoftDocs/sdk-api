---
UID: NF:commoncontrols.IImageList.SetBkColor
title: IImageList::SetBkColor
author: windows-sdk-content
description: Sets the background color for an image list.
old-location: controls\IImageList_SetBkColor.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\setbkcolor.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IImageList interface [Windows Controls],SetBkColor method, IImageList.SetBkColor, IImageList::SetBkColor, SetBkColor, SetBkColor method [Windows Controls], SetBkColor method [Windows Controls],IImageList interface, comctl_IImageList_SetBkColor, comctl_IImageList_SetBkColor_cpp, commoncontrols/IImageList::SetBkColor, controls.IImageList_SetBkColor, controls.comctl_IImageList_SetBkColor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CommonControls.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList.SetBkColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageList::SetBkColor


## -description


Sets the background color for an image list. This method only functions if you add an icon to the image list or use the <a href="https://msdn.microsoft.com/e4953332-e351-4f75-a128-bed98ab9adb4">IImageList::AddMasked</a> method to add a black and white bitmap. Without a mask, the entire image draws, and the background color is not visible. 
		


## -parameters




### -param clrBk [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

The background color to set. If this parameter is set to CLR_NONE, then images draw transparently using the <a href="https://msdn.microsoft.com/e4953332-e351-4f75-a128-bed98ab9adb4">mask</a>.


### -param pclr [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a>*</b>

A pointer to a <b>COLORREF</b> that contains the previous background color on return if successful, or CLR_NONE otherwise.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>IImageList::SetBkColor</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



