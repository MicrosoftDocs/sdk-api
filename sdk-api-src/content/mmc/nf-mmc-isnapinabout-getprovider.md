---
UID: NF:mmc.ISnapinAbout.GetProvider
title: ISnapinAbout::GetProvider
author: windows-sdk-content
description: The ISnapinAbout::GetProvider method enables the console to obtain the snap-in provider name.
old-location: mmc\isnapinabout_getprovider.htm
tech.root: mmc
ms.assetid: a1e0d99c-3485-4a24-aff0-7391ec5f8f6b
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: GetProvider, GetProvider method [MMC], GetProvider method [MMC],ISnapinAbout interface, ISnapinAbout interface [MMC],GetProvider method, ISnapinAbout.GetProvider, ISnapinAbout::GetProvider, _slate_isnapinabout_getprovider, mmc.isnapinabout_getprovider, mmc/ISnapinAbout::GetProvider
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
 - ISnapinAbout.GetProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="_com_cotaskmemalloc">CoTaskMemAlloc</a>.




## -see-also




<a href="https://msdn.microsoft.com/39732334-f849-433b-a313-0c4a675bf408">ISnapinAbout</a>
 

 

