---
UID: NF:iads.IADsObjectOptions.GetOption
title: IADsObjectOptions::GetOption (iads.h)
description: Gets a provider-specific option for a directory object.
helpviewer_keywords: ["GetOption","GetOption method [ADSI]","GetOption method [ADSI]","IADsObjectOptions interface","IADsObjectOptions interface [ADSI]","GetOption method","IADsObjectOptions.GetOption","IADsObjectOptions::GetOption","_ds_iadsobjectoptions_getoption","adsi.iadsobjectoptions__getoption","adsi.iadsobjectoptions_getoption","iads/IADsObjectOptions::GetOption"]
old-location: adsi\iadsobjectoptions_getoption.htm
tech.root: adsi
ms.assetid: 77a994d2-81ae-4afb-be5c-be8d7159a2c2
ms.date: 12/05/2018
ms.keywords: GetOption, GetOption method [ADSI], GetOption method [ADSI],IADsObjectOptions interface, IADsObjectOptions interface [ADSI],GetOption method, IADsObjectOptions.GetOption, IADsObjectOptions::GetOption, _ds_iadsobjectoptions_getoption, adsi.iadsobjectoptions__getoption, adsi.iadsobjectoptions_getoption, iads/IADsObjectOptions::GetOption
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
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsObjectOptions::GetOption
 - iads/IADsObjectOptions::GetOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsObjectOptions.GetOption
---

# IADsObjectOptions::GetOption


## -description

The <b>IADsOptions.GetOption</b> method gets a provider-specific option for a directory object.

## -parameters

### -param lnOption

Indicates the provider-specific option to get. This parameter can be any value in the  <a href="/windows/win32/api/iads/ne-iads-ads_option_enum">ADS_OPTION_ENUM</a> enumeration.

### -param pvValue

Pointer to a <b>VARIANT</b> variable that receives the current value for the option specified in the <i>lnOption</i> parameter.

## -returns

The method supports the standard return values, including <b>S_OK</b> if the operation is successful, and <b>E_ADS_BAD_PARAMETER</b> if the user has supplied an invalid <i>pvValue</i> parameter. For more information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/win32/api/iads/ne-iads-ads_option_enum">ADS_OPTION_ENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsobjectoptions">IADsObjectOptions</a>