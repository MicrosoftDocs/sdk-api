---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0026
title: ADS_PASSWORD_ENCODING_ENUM
author: windows-sdk-content
description: Identifies the type of password encoding used with the ADS_OPTION_PASSWORD_METHOD option in the IADsObjectOptions::GetOption and IADsObjectOptions::SetOption methods.
old-location: adsi\ads_password_encoding_enum.htm
tech.root: adsi
ms.assetid: 0e50790c-a277-4bd4-811a-b794add1afb2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ADS_PASSWORD_ENCODE_CLEAR, ADS_PASSWORD_ENCODE_REQUIRE_SSL, ADS_PASSWORD_ENCODING_ENUM, ADS_PASSWORD_ENCODING_ENUM enumeration [ADSI], adsi.ads_password_encoding_enum, iads/ADS_PASSWORD_ENCODE_CLEAR, iads/ADS_PASSWORD_ENCODE_REQUIRE_SSL, iads/ADS_PASSWORD_ENCODING_ENUM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: iads.h
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
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_PASSWORD_ENCODING_ENUM
product: Windows
targetos: Windows
req.typenames: ADS_PASSWORD_ENCODING_ENUM
req.redist: 
---

# ADS_PASSWORD_ENCODING_ENUM enumeration


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
 

 

