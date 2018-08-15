---
UID: NF:mmc.ISnapinAbout.GetSnapinImage
title: ISnapinAbout::GetSnapinImage
author: windows-sdk-content
description: Enables the console to obtain the snap-in's main icon to be used in the About box.
old-location: mmc\isnapinabout_getsnapinimage.htm
old-project: MMC
ms.assetid: 0a009125-fee0-4ea4-9778-e28797e47465
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetSnapinImage, GetSnapinImage method [MMC], GetSnapinImage method [MMC],ISnapinAbout interface, ISnapinAbout interface [MMC],GetSnapinImage method, ISnapinAbout.GetSnapinImage, ISnapinAbout::GetSnapinImage, _slate_isnapinabout_getsnapinimage, mmc.isnapinabout_getsnapinimage, mmc/ISnapinAbout::GetSnapinImage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - ISnapinAbout.GetSnapinImage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/39732334-f849-433b-a313-0c4a675bf408">ISnapinAbout</a>
 

 

