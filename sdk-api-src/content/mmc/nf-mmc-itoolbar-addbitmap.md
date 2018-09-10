---
UID: NF:mmc.IToolbar.AddBitmap
title: IToolbar::AddBitmap
author: windows-sdk-content
description: Enables a snap-in to add an image to the toolbar.
old-location: mmc\itoolbar_addbitmap.htm
tech.root: mmc
ms.assetid: f2ef31a7-61ce-4ac6-814a-c3a46964c4f1
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: AddBitmap, AddBitmap method [MMC], AddBitmap method [MMC],IToolbar interface, IToolbar interface [MMC],AddBitmap method, IToolbar.AddBitmap, IToolbar::AddBitmap, _slate_itoolbar_addbitmap, mmc.itoolbar_addbitmap, mmc/IToolbar::AddBitmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IToolbar.AddBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IToolbar::AddBitmap


## -description


The <b>IToolbar::AddBitmap</b> method enables a snap-in to add an image to the toolbar.


## -parameters




### -param nImages [in]

An index of images that are available. A value that specifies the number of images in the bitmap being passed in hbmp.


### -param hbmp [in]

A handle to the bitmap to be added to the toolbar.

<div class="alert"><b>Note</b>  The snap-in owns this resource and must free it. A memory leak will occur if the snap-in does not free hbmp.</div>
<div> </div>

### -param cxSize [in]

The height, in pixels, of the bitmap to be added. (In version 1.0, MMC only supported a cxSize of 16.)


### -param cySize [in]

The width, in pixels, of the bitmap to be added. (In version 1.0, MMC only supported a cySize of 16.)


### -param crMask [in]

The color used to generate a mask to overlay the images on the toolbar buttons.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/cf9c9fe9-f58f-47f0-9051-86a514df0c6d">IToolbar</a>
 

 

