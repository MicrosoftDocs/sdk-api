---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0026
title: ADS_PASSWORD_ENCODING_ENUM (iads.h)
description: Identifies the type of password encoding used with the ADS_OPTION_PASSWORD_METHOD option in the IADsObjectOptions::GetOption and IADsObjectOptions::SetOption methods.
helpviewer_keywords: ["ADS_PASSWORD_ENCODE_CLEAR","ADS_PASSWORD_ENCODE_REQUIRE_SSL","ADS_PASSWORD_ENCODING_ENUM","ADS_PASSWORD_ENCODING_ENUM enumeration [ADSI]","adsi.ads_password_encoding_enum","iads/ADS_PASSWORD_ENCODE_CLEAR","iads/ADS_PASSWORD_ENCODE_REQUIRE_SSL","iads/ADS_PASSWORD_ENCODING_ENUM"]
old-location: adsi\ads_password_encoding_enum.htm
tech.root: adsi
ms.assetid: 0e50790c-a277-4bd4-811a-b794add1afb2
ms.date: 12/05/2018
ms.keywords: ADS_PASSWORD_ENCODE_CLEAR, ADS_PASSWORD_ENCODE_REQUIRE_SSL, ADS_PASSWORD_ENCODING_ENUM, ADS_PASSWORD_ENCODING_ENUM enumeration [ADSI], adsi.ads_password_encoding_enum, iads/ADS_PASSWORD_ENCODE_CLEAR, iads/ADS_PASSWORD_ENCODE_REQUIRE_SSL, iads/ADS_PASSWORD_ENCODING_ENUM
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
targetos: Windows
req.typenames: ADS_PASSWORD_ENCODING_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0026
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0026
 - ADS_PASSWORD_ENCODING_ENUM
 - iads/ADS_PASSWORD_ENCODING_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_PASSWORD_ENCODING_ENUM
---

# ADS_PASSWORD_ENCODING_ENUM enumeration


## -description

The <b>ADS_PASSWORD_ENCODING_ENUM</b> enumeration identifies the type of password encoding used with the <b>ADS_OPTION_PASSWORD_METHOD</b> option in the <a href="/windows/desktop/api/iads/nf-iads-iadsobjectoptions-getoption">IADsObjectOptions::GetOption</a> and <a href="/windows/desktop/api/iads/nf-iads-iadsobjectoptions-setoption">IADsObjectOptions::SetOption</a> methods.

## -enum-fields

### -field ADS_PASSWORD_ENCODE_REQUIRE_SSL:0

Passwords are encoded using SSL.

### -field ADS_PASSWORD_ENCODE_CLEAR:1

Passwords are not encoded and are transmitted in plaintext.

## -see-also

<a href="/windows/win32/api/iads/ne-iads-ads_option_enum">ADS_OPTION_ENUM</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsobjectoptions-getoption">IADsObjectOptions::GetOption</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsobjectoptions-setoption">IADsObjectOptions::SetOption</a>
