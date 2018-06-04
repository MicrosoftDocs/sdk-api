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

# __MIDL___MIDL_itf_ads_0000_0000_0026 enumeration


## -description


The <b>ADS_PASSWORD_ENCODING_ENUM</b> enumeration identifies the type of password encoding used with the <b>ADS_OPTION_PASSWORD_METHOD</b> option in the <a href="https://msdn.microsoft.com/77a994d2-81ae-4afb-be5c-be8d7159a2c2">IADsObjectOptions::GetOption</a> and <a href="https://msdn.microsoft.com/e6e43c99-fc8b-4f34-82cf-8cf30c506859">IADsObjectOptions::SetOption</a> methods.


## -enum-fields




### -field ADS_PASSWORD_ENCODE_REQUIRE_SSL

Passwords are encoded using SSL.


### -field ADS_PASSWORD_ENCODE_CLEAR

Passwords are not encoded and are transmitted in plaintext.


## -see-also




<a href="https://msdn.microsoft.com/afb32e03-7e4e-4df9-87c7-db962d62e5f0">ADS_OPTION_ENUM</a>



<a href="https://msdn.microsoft.com/77a994d2-81ae-4afb-be5c-be8d7159a2c2">IADsObjectOptions::GetOption</a>



<a href="https://msdn.microsoft.com/e6e43c99-fc8b-4f34-82cf-8cf30c506859">IADsObjectOptions::SetOption</a>
 

 

