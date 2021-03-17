---
UID: NF:wpcapi.IWPCProviderConfig.GetUserSummary
title: IWPCProviderConfig::GetUserSummary (wpcapi.h)
description: Retrieves the information for each user by using the Parental Controls Control Panel.
helpviewer_keywords: ["GetUserSummary","GetUserSummary method","GetUserSummary method","IWPCProviderConfig interface","IWPCProviderConfig interface","GetUserSummary method","IWPCProviderConfig.GetUserSummary","IWPCProviderConfig::GetUserSummary","parcon.iwpcproviderconfig_getusersummary","wpcapi/IWPCProviderConfig::GetUserSummary"]
old-location: parcon\iwpcproviderconfig_getusersummary.htm
tech.root: parcon
ms.assetid: 89d70aef-9bca-4984-99d1-082041257393
ms.date: 12/05/2018
ms.keywords: GetUserSummary, GetUserSummary method, GetUserSummary method,IWPCProviderConfig interface, IWPCProviderConfig interface,GetUserSummary method, IWPCProviderConfig.GetUserSummary, IWPCProviderConfig::GetUserSummary, parcon.iwpcproviderconfig_getusersummary, wpcapi/IWPCProviderConfig::GetUserSummary
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wpcprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWPCProviderConfig::GetUserSummary
 - wpcapi/IWPCProviderConfig::GetUserSummary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWPCProviderConfig.GetUserSummary
---

# IWPCProviderConfig::GetUserSummary


## -description

Retrieves the information for each user by using the Parental Controls Control Panel. This interface is implemented by third parties.

## -parameters

### -param bstrSID [in]

A string that contains the <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) of the user whose settings you want to obtain.

### -param pbstrUserSummary [out]

A pointer to a string that contains the summary details for the user specified in the <i>bstrSID</i> parameter.

## -returns

If the method succeeds, the function returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The user summary string is used to display information under each user in the Parental Controls Control Panel.

## -see-also

<a href="/windows/desktop/api/wpcapi/nn-wpcapi-iwpcproviderconfig">IWPCProviderConfig</a>