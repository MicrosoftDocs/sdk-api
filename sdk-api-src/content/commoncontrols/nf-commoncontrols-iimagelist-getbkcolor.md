---
UID: NF:commoncontrols.IImageList.GetBkColor
title: IImageList::GetBkColor
author: windows-sdk-content
description: Gets the current background color for an image list.
old-location: controls\IImageList_GetBkColor.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\getbkcolor.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetBkColor, GetBkColor method [Windows Controls], GetBkColor method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetBkColor method, IImageList.GetBkColor, IImageList::GetBkColor, comctl_IImageList_GetBkColor, comctl_IImageList_GetBkColor_cpp, commoncontrols/IImageList::GetBkColor, controls.IImageList_GetBkColor, controls.comctl_IImageList_GetBkColor
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
 - IImageList.GetBkColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageList::GetBkColor


## -description


Gets the current background color for an image list. 
		


## -parameters




### -param pclr [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> that contains the background color when the method returns. 
				


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>IImageList::GetBkColor</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



