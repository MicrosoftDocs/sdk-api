---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# TAPI_TONEMODE enumeration


## -description


The <b>TAPI_TONEMODE</b> enum is used to describe the different selections that are used when generating line tones.


## -enum-fields




### -field TTM_RINGBACK

The tone is a ringback tone. Exact definition is service-provider defined.


### -field TTM_BUSY

The tone is a busy tone. Exact definition is service-provider defined.


### -field TTM_BEEP

The tone is a beep, such as that used to announce the beginning of a recording. Exact definition is service-provider defined.


### -field TTM_BILLING

The tone is a billing information tone, such as a credit card prompt tone. Exact definition is service-provider defined.


## -see-also




<a href="https://msdn.microsoft.com/4c77ee53-3c40-4fdc-9a35-40a8e74b4ec4">ITLegacyCallMediaControl2::GenerateTone</a>
 

 

