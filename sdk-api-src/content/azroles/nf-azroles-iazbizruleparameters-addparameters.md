---
UID: NF:azroles.IAzBizRuleParameters.AddParameters
title: IAzBizRuleParameters::AddParameters (azroles.h)
description: Adds parameters to the list of parameters available to business rule (BizRule) scripts.
helpviewer_keywords: ["AddParameters","AddParameters method [Security]","AddParameters method [Security]","IAzBizRuleParameters interface","IAzBizRuleParameters interface [Security]","AddParameters method","IAzBizRuleParameters.AddParameters","IAzBizRuleParameters::AddParameters","azroles/IAzBizRuleParameters::AddParameters","security.iazbizruleparameters_addparameters_method"]
old-location: security\iazbizruleparameters_addparameters_method.htm
tech.root: security
ms.assetid: ebf336a9-a64a-4ded-b508-56491ebf48e2
ms.date: 12/05/2018
ms.keywords: AddParameters, AddParameters method [Security], AddParameters method [Security],IAzBizRuleParameters interface, IAzBizRuleParameters interface [Security],AddParameters method, IAzBizRuleParameters.AddParameters, IAzBizRuleParameters::AddParameters, azroles/IAzBizRuleParameters::AddParameters, security.iazbizruleparameters_addparameters_method
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
 - IAzBizRuleParameters::AddParameters
 - azroles/IAzBizRuleParameters::AddParameters
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
 - IAzBizRuleParameters.AddParameters
---

# IAzBizRuleParameters::AddParameters


## -description

The <b>AddParameters</b> method adds  parameters to the list of parameters available to business rule (BizRule) scripts.

## -parameters

### -param varParameterNames [in]

The parameter names. This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the  JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a parameter name. This array must be sorted alphabetically; the sort order is as defined by a case-sensitive <a href="/windows/desktop/api/oleauto/nf-oleauto-varcmp">VarCmp</a>. The order of the <i>varParameterValues</i> array must match the order of this array.

### -param varParameterValues [in]

The values of the parameters that are available to BizRule scripts. This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the  JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds a value that corresponds to an element in the <i>varParameterNames</i> array. The default value is <b>VT_NULL</b>. The entries in the array can hold any type except <b>VT_UNKNOWN</b> and <b>VT_DISPATCH</b>.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/azroles/nn-azroles-iazbizruleparameters">IAzBizRuleParameters</a>



<a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext3-get_bizruleparameters">IAzClientContext3::BizRuleParameters</a>