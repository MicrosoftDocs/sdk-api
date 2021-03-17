---
UID: NF:iads.IADsObjectOptions.SetOption
title: IADsObjectOptions::SetOption (iads.h)
description: Sets a provider-specific option for manipulating a directory object.
helpviewer_keywords: ["IADsObjectOptions interface [ADSI]","SetOption method","IADsObjectOptions.SetOption","IADsObjectOptions::SetOption","SetOption","SetOption method [ADSI]","SetOption method [ADSI]","IADsObjectOptions interface","_ds_iadsobjectoptions_setoption","adsi.iadsobjectoptions__setoption","adsi.iadsobjectoptions_setoption","iads/IADsObjectOptions::SetOption"]
old-location: adsi\iadsobjectoptions_setoption.htm
tech.root: adsi
ms.assetid: e6e43c99-fc8b-4f34-82cf-8cf30c506859
ms.date: 12/05/2018
ms.keywords: IADsObjectOptions interface [ADSI],SetOption method, IADsObjectOptions.SetOption, IADsObjectOptions::SetOption, SetOption, SetOption method [ADSI], SetOption method [ADSI],IADsObjectOptions interface, _ds_iadsobjectoptions_setoption, adsi.iadsobjectoptions__setoption, adsi.iadsobjectoptions_setoption, iads/IADsObjectOptions::SetOption
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
 - IADsObjectOptions::SetOption
 - iads/IADsObjectOptions::SetOption
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
 - IADsObjectOptions.SetOption
---

# IADsObjectOptions::SetOption


## -description

The <b>IADsOptions.SetOption</b> method sets a provider-specific option for manipulating a directory object.

## -parameters

### -param lnOption

Indicates the provider-specific option to set. This parameter can be any value in the  <a href="/windows/win32/api/iads/ne-iads-ads_option_enum">ADS_OPTION_ENUM</a> enumeration except <b>ADS_OPTION_SERVERNAME</b> or <b>ADS_OPTION_MUTUAL_AUTH_STATUS</b>.

### -param vValue

Specifies the value to set for the option specified in the <i>lnOption</i> parameter.

## -returns

The method supports the standard return values, including <b>S_OK</b> for a successful operation and <b>E_ADS_BAD_PARAMETER</b> when the user has supplied an invalid <i>pValue</i> parameter. For more information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsobjectoptions">IADsObjectOptions</a>