---
UID: NF:azroles.IAzBizRuleParameters.RemoveAll
title: IAzBizRuleParameters::RemoveAll (azroles.h)
description: Removes all parameters from the list of parameters available to business rule (BizRule) scripts.
helpviewer_keywords: ["IAzBizRuleParameters interface [Security]","RemoveAll method","IAzBizRuleParameters.RemoveAll","IAzBizRuleParameters::RemoveAll","RemoveAll","RemoveAll method [Security]","RemoveAll method [Security]","IAzBizRuleParameters interface","azroles/IAzBizRuleParameters::RemoveAll","security.iazbizruleparameters_removeall_method"]
old-location: security\iazbizruleparameters_removeall_method.htm
tech.root: security
ms.assetid: 5ec13e1b-6b83-4178-a5a5-b278fe7c8c3c
ms.date: 03/20/2023
ms.keywords: IAzBizRuleParameters interface [Security],RemoveAll method, IAzBizRuleParameters.RemoveAll, IAzBizRuleParameters::RemoveAll, RemoveAll, RemoveAll method [Security], RemoveAll method [Security],IAzBizRuleParameters interface, azroles/IAzBizRuleParameters::RemoveAll, security.iazbizruleparameters_removeall_method
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
 - IAzBizRuleParameters::RemoveAll
 - azroles/IAzBizRuleParameters::RemoveAll
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
 - IAzBizRuleParameters.RemoveAll
---

# IAzBizRuleParameters::RemoveAll

## -description

The **IAzBizRuleParameters::RemoveAll** method removes all parameters from the list of parameters available to business rule (BizRule) scripts.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -see-also

[IAzBizRuleParameters](nn-azroles-iazbizruleparameters.md)

[IAzClientContext3::BizRuleParameters](nf-azroles-iazclientcontext3-get_bizruleparameters.md)
