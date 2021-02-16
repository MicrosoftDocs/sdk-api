---
UID: NF:wsdbase.IWSDHttpAuthParameters.GetClientAccessToken
title: IWSDHttpAuthParameters::GetClientAccessToken (wsdbase.h)
description: GetClientAccessToken method retrieves the client access token that can be used to either authenticate or impersonate the client.
helpviewer_keywords: ["GetClientAccessToken","GetClientAccessToken method","GetClientAccessToken method","IWSDHttpAuthParameters interface","IWSDHttpAuthParameters interface","GetClientAccessToken method","IWSDHttpAuthParameters.GetClientAccessToken","IWSDHttpAuthParameters::GetClientAccessToken","ncd.iwsdhttpauthparameters_getclientaccesstoken","wsdbase/IWSDHttpAuthParameters::GetClientAccessToken"]
old-location: ncd\iwsdhttpauthparameters_getclientaccesstoken.htm
tech.root: ncd
ms.assetid: 8E214497-151C-486B-8FE9-7B481AD403F9
ms.date: 12/05/2018
ms.keywords: GetClientAccessToken, GetClientAccessToken method, GetClientAccessToken method,IWSDHttpAuthParameters interface, IWSDHttpAuthParameters interface,GetClientAccessToken method, IWSDHttpAuthParameters.GetClientAccessToken, IWSDHttpAuthParameters::GetClientAccessToken, ncd.iwsdhttpauthparameters_getclientaccesstoken, wsdbase/IWSDHttpAuthParameters::GetClientAccessToken
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDHttpAuthParameters::GetClientAccessToken
 - wsdbase/IWSDHttpAuthParameters::GetClientAccessToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdbase.h
api_name:
 - IWSDHttpAuthParameters.GetClientAccessToken
---

# IWSDHttpAuthParameters::GetClientAccessToken


## -description

The <b>GetClientAccessToken</b> method retrieves the client access token that can be used to either authenticate or impersonate the client.

## -parameters

### -param phToken [out]

Pointer to a variable that on return receives the token handle.

## -returns

This method returns S_OK on success.

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpauthparameters">IWSDHttpAuthParameters</a>