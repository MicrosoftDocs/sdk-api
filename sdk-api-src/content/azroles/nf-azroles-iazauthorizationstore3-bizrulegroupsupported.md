---
UID: NF:azroles.IAzAuthorizationStore3.BizruleGroupSupported
title: IAzAuthorizationStore3::BizruleGroupSupported (azroles.h)
description: Returns a Boolean value that specifies whether this IAzAuthorizationStore3 object supports application groups that use business rule (BizRule) scripts.
helpviewer_keywords: ["BizruleGroupSupported","BizruleGroupSupported method [Security]","BizruleGroupSupported method [Security]","IAzAuthorizationStore3 interface","IAzAuthorizationStore3 interface [Security]","BizruleGroupSupported method","IAzAuthorizationStore3.BizruleGroupSupported","IAzAuthorizationStore3::BizruleGroupSupported","azroles/IAzAuthorizationStore3::BizruleGroupSupported","security.iazauthorizationstore3_bizrulegroupsupported_method"]
old-location: security\iazauthorizationstore3_bizrulegroupsupported_method.htm
tech.root: security
ms.assetid: 88449b12-5086-4f86-94d4-2a4afb4be070
ms.date: 12/05/2018
ms.keywords: BizruleGroupSupported, BizruleGroupSupported method [Security], BizruleGroupSupported method [Security],IAzAuthorizationStore3 interface, IAzAuthorizationStore3 interface [Security],BizruleGroupSupported method, IAzAuthorizationStore3.BizruleGroupSupported, IAzAuthorizationStore3::BizruleGroupSupported, azroles/IAzAuthorizationStore3::BizruleGroupSupported, security.iazauthorizationstore3_bizrulegroupsupported_method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
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
 - IAzAuthorizationStore3::BizruleGroupSupported
 - azroles/IAzAuthorizationStore3::BizruleGroupSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzAuthorizationStore3.BizruleGroupSupported
---

# IAzAuthorizationStore3::BizruleGroupSupported


## -description

The <b>BizruleGroupSupported</b> method returns a Boolean value that specifies whether this <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore3">IAzAuthorizationStore3</a> object supports application groups that use business rule (BizRule) scripts.

## -parameters

### -param pbSupported [out]

<b>VARIANT_TRUE</b> if the current <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore3">IAzAuthorizationStore3</a> object supports scripts that use business logic to determine group membership; otherwise, <b>VARIANT_FALSE</b>.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.