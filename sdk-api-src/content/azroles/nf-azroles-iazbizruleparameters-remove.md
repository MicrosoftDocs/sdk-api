---
UID: NF:azroles.IAzBizRuleParameters.Remove
title: IAzBizRuleParameters::Remove (azroles.h)
description: Removes the specified parameter from the list of parameters available to business rule (BizRule) scripts.
old-location: security\iazbizruleparameters_remove_method.htm
tech.root: SecAuthZ
ms.assetid: 1874ac48-0a06-4387-89c2-c194b60bb8f2
ms.date: 12/05/2018
ms.keywords: IAzBizRuleParameters interface [Security],Remove method, IAzBizRuleParameters.Remove, IAzBizRuleParameters::Remove, Remove, Remove method [Security], Remove method [Security],IAzBizRuleParameters interface, azroles/IAzBizRuleParameters::Remove, security.iazbizruleparameters_remove_method
ms.topic: method
f1_keywords:
- azroles/IAzBizRuleParameters.Remove
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Azroles.h
api_name:
- IAzBizRuleParameters.Remove
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzBizRuleParameters::Remove


## -description


The <b>Remove</b> method removes the specified parameter from the list of parameters available to business rule (BizRule) scripts.


## -parameters




### -param varParameterName [in]

The name of the parameter to remove.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazbizruleparameters">IAzBizRuleParameters</a>



<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext3-get_bizruleparameters">IAzClientContext3::BizRuleParameters</a>
 

 

