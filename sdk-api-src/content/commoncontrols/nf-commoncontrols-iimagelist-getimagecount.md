---
UID: NF:commoncontrols.IImageList.GetImageCount
title: IImageList::GetImageCount (commoncontrols.h)
author: windows-sdk-content
description: Gets the number of images in an image list.
old-location: controls\IImageList_GetImageCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\getimagecount.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetImageCount, GetImageCount method [Windows Controls], GetImageCount method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetImageCount method, IImageList.GetImageCount, IImageList::GetImageCount, comctl_IImageList_GetImageCount, comctl_IImageList_GetImageCount_cpp, commoncontrols/IImageList::GetImageCount, controls.IImageList_GetImageCount, controls.comctl_IImageList_GetImageCount
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
 - IImageList.GetImageCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



To use <b>IImageList::GetImageCount</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



