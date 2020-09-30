---
UID: NF:azroles.IAzBizRuleParameters.AddParameter
title: IAzBizRuleParameters::AddParameter (azroles.h)
description: Adds a parameter to the list of parameters available to business rule (BizRule) scripts.
helpviewer_keywords: ["AddParameter","AddParameter method [Security]","AddParameter method [Security]","IAzBizRuleParameters interface","IAzBizRuleParameters interface [Security]","AddParameter method","IAzBizRuleParameters.AddParameter","IAzBizRuleParameters::AddParameter","azroles/IAzBizRuleParameters::AddParameter","security.iazbizruleparameters_addparameter_method"]
old-location: security\iazbizruleparameters_addparameter_method.htm
tech.root: security
ms.assetid: ea5c45d4-34c8-4d7c-a1b2-8f45574d9449
ms.date: 12/05/2018
ms.keywords: AddParameter, AddParameter method [Security], AddParameter method [Security],IAzBizRuleParameters interface, IAzBizRuleParameters interface [Security],AddParameter method, IAzBizRuleParameters.AddParameter, IAzBizRuleParameters::AddParameter, azroles/IAzBizRuleParameters::AddParameter, security.iazbizruleparameters_addparameter_method
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
 - IAzBizRuleParameters::AddParameter
 - azroles/IAzBizRuleParameters::AddParameter
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
 - IAzBizRuleParameters.AddParameter
---

# IAzBizRuleParameters::AddParameter


## -description

The <b>AddParameter</b> method adds a parameter to the list of parameters available to business rule (BizRule) scripts.

## -parameters

### -param bstrParameterName [in]

A string that contains the parameter name.

### -param varParameterValue [in]

The data type of the parameter value.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/azroles/nn-azroles-iazbizruleparameters">IAzBizRuleParameters</a>



<a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext3-get_bizruleparameters">IAzClientContext3::BizRuleParameters</a>