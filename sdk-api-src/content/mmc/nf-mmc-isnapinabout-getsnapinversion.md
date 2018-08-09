---
UID: NF:mmc.ISnapinAbout.GetSnapinVersion
title: ISnapinAbout::GetSnapinVersion
author: windows-sdk-content
description: Enables the console to obtain the snap-in's version number.
old-location: mmc\isnapinabout_getsnapinversion.htm
old-project: MMC
ms.assetid: c933bb14-cf07-4eca-9a97-c833ed5f5438
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetSnapinVersion, GetSnapinVersion method [MMC], GetSnapinVersion method [MMC],ISnapinAbout interface, ISnapinAbout interface [MMC],GetSnapinVersion method, ISnapinAbout.GetSnapinVersion, ISnapinAbout::GetSnapinVersion, _slate_isnapinabout_getsnapinversion, mmc.isnapinabout_getsnapinversion, mmc/ISnapinAbout::GetSnapinVersion
ms.prod: windows
ms.technology: windows-sdk
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
 - ISnapinAbout.GetSnapinVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ISnapinAbout::GetSnapinVersion


## -description


The ISnapinAbout::GetSnapinVersion method enables the console to obtain the snap-in's version number.


## -parameters




### -param lpVersion [out]

A pointer to the text of the snap-in version number.


## -returns



This method can return one of these values.




## -remarks



Memory for out parameters must be allocated using the COM function 
<a href="_com_cotaskmemalloc">CoTaskMemAlloc</a>.




## -see-also




<a href="https://msdn.microsoft.com/39732334-f849-433b-a313-0c4a675bf408">ISnapinAbout</a>
 

 

