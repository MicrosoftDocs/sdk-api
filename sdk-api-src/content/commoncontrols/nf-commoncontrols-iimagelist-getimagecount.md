---
UID: NF:commoncontrols.IImageList.GetImageCount
title: IImageList::GetImageCount
author: windows-sdk-content
description: Gets the number of images in an image list.
old-location: controls\IImageList_GetImageCount.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\getimagecount.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetImageCount, GetImageCount method [Windows Controls], GetImageCount method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetImageCount method, IImageList.GetImageCount, IImageList::GetImageCount, comctl_IImageList_GetImageCount, comctl_IImageList_GetImageCount_cpp, commoncontrols/IImageList::GetImageCount, controls.IImageList_GetImageCount, controls.comctl_IImageList_GetImageCount
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: OFNOTIFYW, *LPOFNOTIFYW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList.GetImageCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList::GetImageCount


## -description



		Gets the number of images in an image list. 
		


## -parameters




### -param pi [out]

Type: <b>int*</b>

A pointer to an <b>int</b> that contains the number of images when the method returns.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>IImageList::GetImageCount</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



