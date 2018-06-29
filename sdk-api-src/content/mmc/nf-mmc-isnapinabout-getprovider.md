---
UID: NF:mmc.ISnapinAbout.GetProvider
title: ISnapinAbout::GetProvider
author: windows-sdk-content
description: The ISnapinAbout::GetProvider method enables the console to obtain the snap-in provider name.
old-location: mmc\isnapinabout_getprovider.htm
old-project: MMC
ms.assetid: a1e0d99c-3485-4a24-aff0-7391ec5f8f6b
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: GetProvider, GetProvider method [MMC], GetProvider method [MMC],ISnapinAbout interface, ISnapinAbout interface [MMC],GetProvider method, ISnapinAbout.GetProvider, ISnapinAbout::GetProvider, _slate_isnapinabout_getprovider, mmc.isnapinabout_getprovider, mmc/ISnapinAbout::GetProvider
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
 - ISnapinAbout.GetProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ISnapinAbout::GetProvider


## -description


The <b>ISnapinAbout::GetProvider</b> method enables the console to obtain the snap-in provider name.


## -parameters




### -param lpName [out]

A pointer to the text of the snap-in provider name.


## -returns



This method can return one of these values.




## -remarks



Memory for out parameters must be allocated using the COM API function 
<a href="https://msdn.microsoft.com/library/ms692727(v=VS.85).aspx">CoTaskMemAlloc</a>.




## -see-also




<a href="https://msdn.microsoft.com/39732334-f849-433b-a313-0c4a675bf408">ISnapinAbout</a>
 

 

