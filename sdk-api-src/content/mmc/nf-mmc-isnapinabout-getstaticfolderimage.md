---
UID: NF:mmc.ISnapinAbout.GetStaticFolderImage
title: ISnapinAbout::GetStaticFolderImage
author: windows-sdk-content
description: The ISnapinAbout::GetStaticFolderImage method allows the console to obtain the static folder images for the scope and result panes.
old-location: mmc\isnapinabout_getstaticfolderimage.htm
tech.root: mmc
ms.assetid: 87be74e1-67d4-4205-a12a-f4fd1b22f038
ms.author: windowssdkdev
ms.date: 09/04/2018
ms.keywords: GetStaticFolderImage, GetStaticFolderImage method [MMC], GetStaticFolderImage method [MMC],ISnapinAbout interface, ISnapinAbout interface [MMC],GetStaticFolderImage method, ISnapinAbout.GetStaticFolderImage, ISnapinAbout::GetStaticFolderImage, _slate_isnapinabout_getstaticfolderimage, mmc.isnapinabout_getstaticfolderimage, mmc/ISnapinAbout::GetStaticFolderImage
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - ISnapinAbout.GetStaticFolderImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISnapinAbout::GetStaticFolderImage


## -description


The <b>ISnapinAbout::GetStaticFolderImage</b> method allows the console to obtain the static folder images for the scope and result panes.


## -parameters




### -param hSmallImage [out]

A pointer to the handle to a small icon (16x16 pixels) in either the scope or result view pane.


### -param hSmallImageOpen [out]

A pointer to the handle to a small open-folder icon (16x16 pixels).


### -param hLargeImage [out]

A pointer to the handle to a large icon (32x32 pixels).


### -param cMask [out]

A pointer to a 
COLORREF structure that specifies the color used to generate a mask.


## -returns



This method can return one of these values.




## -remarks



MMC creates copies of the returned bitmaps. The snap-in can free the originals when the 
ISnapinAbout interface is released.

MMC uses default static folder images and icons if it cannot obtain the snap-in icons.




## -see-also




<a href="https://msdn.microsoft.com/39732334-f849-433b-a313-0c4a675bf408">ISnapinAbout</a>
 

 

