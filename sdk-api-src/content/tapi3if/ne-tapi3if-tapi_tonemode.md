---
UID: NE:tapi3if.TAPI_TONEMODE
title: TAPI_TONEMODE
author: windows-sdk-content
description: The TAPI_TONEMODE enum is used to describe the different selections that are used when generating line tones.
old-location: tapi3\tapi_tonemode.htm
old-project: tapi
ms.assetid: eeae9d4a-824c-4316-8eb3-846563ac4a54
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: TAPI_TONEMODE, TAPI_TONEMODE enumeration [TAPI 2.2], TTM_BEEP, TTM_BILLING, TTM_BUSY, TTM_RINGBACK, _tapi3_tapi_tonemode, tapi3.tapi_tonemode, tapi3if/TAPI_TONEMODE, tapi3if/TTM_BEEP, tapi3if/TTM_BILLING, tapi3if/TTM_BUSY, tapi3if/TTM_RINGBACK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: TAPI_TONEMODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - TAPI_TONEMODE
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

