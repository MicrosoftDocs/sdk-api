---
UID: NF:xblidpauthmanager.IXblIdpAuthManager.GetTokenAndSignatureWithTokenResult
title: IXblIdpAuthManager::GetTokenAndSignatureWithTokenResult
author: windows-sdk-content
description: Reserved for Microsoft use.
old-location: xblidp\ixblidpauthmanager_gettokenandsignaturewithtokenresult.htm
old-project: xblidp
ms.assetid: 22ACC545-8EDE-4009-9EE9-1AE541985E6A
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetTokenAndSignatureWithTokenResult, GetTokenAndSignatureWithTokenResult method, GetTokenAndSignatureWithTokenResult method,IXblIdpAuthManager interface, IXblIdpAuthManager interface,GetTokenAndSignatureWithTokenResult method, IXblIdpAuthManager.GetTokenAndSignatureWithTokenResult, IXblIdpAuthManager::GetTokenAndSignatureWithTokenResult, xblidp.ixblidpauthmanager_gettokenandsignaturewithtokenresult, xblidpauthmanager/IXblIdpAuthManager::GetTokenAndSignatureWithTokenResult
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	XblIdpAuthManager.h
api_name:
-	IXblIdpAuthManager.GetTokenAndSignatureWithTokenResult
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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
 

 

