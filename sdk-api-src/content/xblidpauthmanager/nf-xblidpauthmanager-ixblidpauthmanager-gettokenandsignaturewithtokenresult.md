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

# IXblIdpAuthManager::GetTokenAndSignatureWithTokenResult


## -description


Reserved for Microsoft use.


## -parameters




### -param msaAccountId

Type: <b>__RPC__in_opt_string</b>


### -param appSid

Type: <b>__RPC__in_string</b>


### -param msaTarget

Type: <b>__RPC__in_string</b>


### -param msaPolicy

Type: <b>__RPC__in_string</b>


### -param httpMethod

Type: <b>__RPC__in_string</b>


### -param uri

Type: <b>__RPC__in_string</b>


### -param headers

Type: <b>__RPC__in_opt_string</b>


### -param body




### -param bodySize

Type: <b>__RPC__in_ecount_full_opt</b>


### -param forceRefresh




### -param result






## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/BD421B26-241F-46C4-9B77-ADCFFBEA24B0">IXblIdpAuthManager</a>
 

 

