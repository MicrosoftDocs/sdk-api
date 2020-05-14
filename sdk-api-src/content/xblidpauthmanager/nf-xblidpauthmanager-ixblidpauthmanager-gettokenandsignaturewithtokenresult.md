---
UID: NF:xblidpauthmanager.IXblIdpAuthManager.GetTokenAndSignatureWithTokenResult
title: IXblIdpAuthManager::GetTokenAndSignatureWithTokenResult (xblidpauthmanager.h)
description: Reserved for Microsoft use.helpviewer_keywords: ["GetTokenAndSignatureWithTokenResult","GetTokenAndSignatureWithTokenResult method","GetTokenAndSignatureWithTokenResult method","IXblIdpAuthManager interface","IXblIdpAuthManager interface","GetTokenAndSignatureWithTokenResult method","IXblIdpAuthManager.GetTokenAndSignatureWithTokenResult","IXblIdpAuthManager::GetTokenAndSignatureWithTokenResult","xblidp.ixblidpauthmanager_gettokenandsignaturewithtokenresult","xblidpauthmanager/IXblIdpAuthManager::GetTokenAndSignatureWithTokenResult"]
old-location: xblidp\ixblidpauthmanager_gettokenandsignaturewithtokenresult.htm
tech.root: xblidp
ms.assetid: 22ACC545-8EDE-4009-9EE9-1AE541985E6A
ms.date: 12/05/2018
ms.keywords: GetTokenAndSignatureWithTokenResult, GetTokenAndSignatureWithTokenResult method, GetTokenAndSignatureWithTokenResult method,IXblIdpAuthManager interface, IXblIdpAuthManager interface,GetTokenAndSignatureWithTokenResult method, IXblIdpAuthManager.GetTokenAndSignatureWithTokenResult, IXblIdpAuthManager::GetTokenAndSignatureWithTokenResult, xblidp.ixblidpauthmanager_gettokenandsignaturewithtokenresult, xblidpauthmanager/IXblIdpAuthManager::GetTokenAndSignatureWithTokenResult
f1_keywords:
- xblidpauthmanager/IXblIdpAuthManager.GetTokenAndSignatureWithTokenResult
dev_langs:
- c++
req.header: xblidpauthmanager.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- XblIdpAuthManager.h
api_name:
- IXblIdpAuthManager.GetTokenAndSignatureWithTokenResult
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Type: <b>BYTE*</b>


### -param bodySize

Type: <b>__RPC__in_ecount_full_opt</b>


### -param forceRefresh

Type: <b>BOOL</b>


### -param result

Type: <b>IXblIdpAuthTokenResult**</b>




## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xblidpauthmanager/nn-xblidpauthmanager-ixblidpauthmanager">IXblIdpAuthManager</a>
 

 

