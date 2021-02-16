---
UID: NF:mmc.ISnapinAbout.GetStaticFolderImage
title: ISnapinAbout::GetStaticFolderImage (mmc.h)
description: The ISnapinAbout::GetStaticFolderImage method allows the console to obtain the static folder images for the scope and result panes.
helpviewer_keywords: ["GetStaticFolderImage","GetStaticFolderImage method [MMC]","GetStaticFolderImage method [MMC]","ISnapinAbout interface","ISnapinAbout interface [MMC]","GetStaticFolderImage method","ISnapinAbout.GetStaticFolderImage","ISnapinAbout::GetStaticFolderImage","_slate_isnapinabout_getstaticfolderimage","mmc.isnapinabout_getstaticfolderimage","mmc/ISnapinAbout::GetStaticFolderImage"]
old-location: mmc\isnapinabout_getstaticfolderimage.htm
tech.root: mmc
ms.assetid: 87be74e1-67d4-4205-a12a-f4fd1b22f038
ms.date: 12/05/2018
ms.keywords: GetStaticFolderImage, GetStaticFolderImage method [MMC], GetStaticFolderImage method [MMC],ISnapinAbout interface, ISnapinAbout interface [MMC],GetStaticFolderImage method, ISnapinAbout.GetStaticFolderImage, ISnapinAbout::GetStaticFolderImage, _slate_isnapinabout_getstaticfolderimage, mmc.isnapinabout_getstaticfolderimage, mmc/ISnapinAbout::GetStaticFolderImage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISnapinAbout::GetStaticFolderImage
 - mmc/ISnapinAbout::GetStaticFolderImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - ISnapinAbout.GetStaticFolderImage
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

<a href="/windows/desktop/api/mmc/nn-mmc-isnapinabout">ISnapinAbout</a>