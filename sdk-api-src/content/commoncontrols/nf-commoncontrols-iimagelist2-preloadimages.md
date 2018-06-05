---
UID: NF:commoncontrols.IImageList2.PreloadImages
title: IImageList2::PreloadImages
author: windows-sdk-content
description: Preloads images, as specified.
old-location: controls\IImageList2_PreloadImages.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\preloadimages.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IImageList2 interface [Windows Controls],PreloadImages method, IImageList2.PreloadImages, IImageList2::PreloadImages, PreloadImages, PreloadImages method [Windows Controls], PreloadImages method [Windows Controls],IImageList2 interface, _shell_IImageList2_PreloadImages, _shell_IImageList2_PreloadImages_cpp, commoncontrols/IImageList2::PreloadImages, controls.IImageList2_PreloadImages, controls._shell_IImageList2_PreloadImages
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Commoncontrols.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OFNOTIFYW, *LPOFNOTIFYW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Comctl32.dll
api_name:
-	IImageList2.PreloadImages
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList2::PreloadImages


## -description


Preloads images, as specified.


## -parameters




### -param pimldp [in]

Type: <b><a href="https://msdn.microsoft.com/c3579946-d690-4f32-9662-b4e1b3f06aba">IMAGELISTDRAWPARAMS</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/c3579946-d690-4f32-9662-b4e1b3f06aba">IMAGELISTDRAWPARAMS</a> structure containing information about an image list draw operation.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



