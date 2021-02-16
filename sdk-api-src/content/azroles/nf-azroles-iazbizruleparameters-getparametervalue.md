---
UID: NF:azroles.IAzBizRuleParameters.GetParameterValue
title: IAzBizRuleParameters::GetParameterValue (azroles.h)
description: Gets the value type of the business rule (BizRule) parameter with the specified name.
helpviewer_keywords: ["GetParameterValue","GetParameterValue method [Security]","GetParameterValue method [Security]","IAzBizRuleParameters interface","IAzBizRuleParameters interface [Security]","GetParameterValue method","IAzBizRuleParameters.GetParameterValue","IAzBizRuleParameters::GetParameterValue","azroles/IAzBizRuleParameters::GetParameterValue","security.iazbizruleparameters_getparametervalue_method"]
old-location: security\iazbizruleparameters_getparametervalue_method.htm
tech.root: security
ms.assetid: 210dc872-0879-4b4f-bdc3-cbb2208dafbe
ms.date: 12/05/2018
ms.keywords: GetParameterValue, GetParameterValue method [Security], GetParameterValue method [Security],IAzBizRuleParameters interface, IAzBizRuleParameters interface [Security],GetParameterValue method, IAzBizRuleParameters.GetParameterValue, IAzBizRuleParameters::GetParameterValue, azroles/IAzBizRuleParameters::GetParameterValue, security.iazbizruleparameters_getparametervalue_method
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
 - IAzBizRuleParameters::GetParameterValue
 - azroles/IAzBizRuleParameters::GetParameterValue
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
 - IAzBizRuleParameters.GetParameterValue
---

# IAzBizRuleParameters::GetParameterValue


## -description

The <b>GetParameterValue</b> method gets the value type of the business rule (BizRule) parameter with the specified name.

## -parameters

### -param bstrParameterName [in]

A string that contains the parameter name.

### -param pvarParameterValue [out]

A pointer to the data type of the parameter value.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/azroles/nn-azroles-iazbizruleparameters">IAzBizRuleParameters</a>



<a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext3-get_bizruleparameters">IAzClientContext3::BizRuleParameters</a>