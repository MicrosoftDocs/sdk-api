---
UID: NF:mmc.ISnapinAbout.GetSnapinImage
title: ISnapinAbout::GetSnapinImage (mmc.h)
description: Enables the console to obtain the snap-in's main icon to be used in the About box.
helpviewer_keywords: ["GetSnapinImage","GetSnapinImage method [MMC]","GetSnapinImage method [MMC]","ISnapinAbout interface","ISnapinAbout interface [MMC]","GetSnapinImage method","ISnapinAbout.GetSnapinImage","ISnapinAbout::GetSnapinImage","_slate_isnapinabout_getsnapinimage","mmc.isnapinabout_getsnapinimage","mmc/ISnapinAbout::GetSnapinImage"]
old-location: mmc\isnapinabout_getsnapinimage.htm
tech.root: mmc
ms.assetid: 0a009125-fee0-4ea4-9778-e28797e47465
ms.date: 12/05/2018
ms.keywords: GetSnapinImage, GetSnapinImage method [MMC], GetSnapinImage method [MMC],ISnapinAbout interface, ISnapinAbout interface [MMC],GetSnapinImage method, ISnapinAbout.GetSnapinImage, ISnapinAbout::GetSnapinImage, _slate_isnapinabout_getsnapinimage, mmc.isnapinabout_getsnapinimage, mmc/ISnapinAbout::GetSnapinImage
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
 - ISnapinAbout::GetSnapinImage
 - mmc/ISnapinAbout::GetSnapinImage
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
 - ISnapinAbout.GetSnapinImage
---

# ISnapinAbout::GetSnapinImage


## -description

The <b>ISnapinAbout::GetSnapinImage</b> method enables the console to obtain the snap-in's main icon to be used in the About box.

## -parameters

### -param hAppIcon [out]

A pointer to the handle to the main icon of the snap-in that is to be used in the About property page.

## -returns

This method can return one of these values.

## -remarks

For bitmaps, MMC requires a specific background color so it can generate a transparency mask. Icons, however, have built-in transparency so MMC does not require a specific background color.

MMC creates a copy of the returned icon. The snap-in can free the icon when the 
ISnapinAbout interface is released.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-isnapinabout">ISnapinAbout</a>