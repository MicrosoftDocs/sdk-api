---
UID: NS:drt.drt_registration_tag
title: drt_registration_tag
author: windows-sdk-content
description: The DRT_REGISTRATION structure contains key and application data that make up a registration.
old-location: p2p\drt_registration.htm
tech.root: p2psdk
ms.assetid: 1b5fea2c-c1df-4639-8f62-e62d8a09b1f5
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PDRT_REGISTRATION, DRT_REGISTRATION, DRT_REGISTRATION structure [Peer Networking], PDRT_REGISTRATION, PDRT_REGISTRATION structure pointer [Peer Networking], drt/DRT_REGISTRATION, drt/PDRT_REGISTRATION, drt_registration_tag, p2p.drt_registration"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - HeaderDef
api_location:
 - drt.h
api_name:
 - DRT_REGISTRATION
product: Windows
targetos: Windows
req.typenames: DRT_REGISTRATION, *PDRT_REGISTRATION
req.redist: 
---

# drt_registration_tag structure


## -description


The <b>DRT_REGISTRATION</b> structure contains  key and application data that make up a registration.


## -struct-fields




### -field key

Contains the key portion of the registration.


### -field appData

The application data associated with the key. The <a href="https://msdn.microsoft.com/ee81daca-e889-471e-b43b-4593380a55dd">DRT_DATA</a> structure containing this application data must point to a buffer less than 4KB in size.


## -see-also




<a href="https://msdn.microsoft.com/23cf713e-2730-456c-a3da-649c5ed00ffb">DRT_SEARCH_RESULT</a>



<a href="https://msdn.microsoft.com/069358e0-4b61-44ed-b235-37f1d038feff">DrtCreateDerivedKey</a>



<a href="https://msdn.microsoft.com/9aa1ee16-648d-4769-a464-4659dea14dba">DrtRegisterKey</a>
 

 

