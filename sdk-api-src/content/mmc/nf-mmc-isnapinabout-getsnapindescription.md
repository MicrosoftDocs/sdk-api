---
UID: NF:mmc.ISnapinAbout.GetSnapinDescription
title: ISnapinAbout::GetSnapinDescription
author: windows-sdk-content
description: Enables the console to obtain the text for the snap-in's description box.
old-location: mmc\isnapinabout_getsnapindescription.htm
old-project: MMC
ms.assetid: 9f97d504-baba-4c9a-ab0b-ef585d2fe12c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetSnapinDescription, GetSnapinDescription method [MMC], GetSnapinDescription method [MMC],ISnapinAbout interface, ISnapinAbout interface [MMC],GetSnapinDescription method, ISnapinAbout.GetSnapinDescription, ISnapinAbout::GetSnapinDescription, _slate_isnapinabout_getsnapindescription, mmc.isnapinabout_getsnapindescription, mmc/ISnapinAbout::GetSnapinDescription
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
 - ISnapinAbout.GetSnapinDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ISnapinAbout::GetSnapinDescription


## -description


The ISnapinAbout::GetSnapinDescription method enables the console to obtain the text for the snap-in's description box.


## -parameters




### -param lpDescription [out]

A pointer to the text for the description box on an <b>About</b> property page.


## -returns



This method can return one of these values.




## -remarks



The description should be limited to four lines of text to fit the description windows on the Snap-in Manager property pages.

Memory for out parameters must be allocated using the COM API function 
<a href="_com_cotaskmemalloc">CoTaskMemAlloc</a>.




## -see-also




<a href="https://msdn.microsoft.com/39732334-f849-433b-a313-0c4a675bf408">ISnapinAbout</a>
 

 

