---
UID: NF:azroles.IAzBizRuleParameters.GetParameterValue
title: IAzBizRuleParameters::GetParameterValue
author: windows-sdk-content
description: Gets the value type of the business rule (BizRule) parameter with the specified name.
old-location: security\iazbizruleparameters_getparametervalue_method.htm
tech.root: secauthz
ms.assetid: 210dc872-0879-4b4f-bdc3-cbb2208dafbe
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetParameterValue, GetParameterValue method [Security], GetParameterValue method [Security],IAzBizRuleParameters interface, IAzBizRuleParameters interface [Security],GetParameterValue method, IAzBizRuleParameters.GetParameterValue, IAzBizRuleParameters::GetParameterValue, azroles/IAzBizRuleParameters::GetParameterValue, security.iazbizruleparameters_getparametervalue_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IAzBizRuleParameters.GetParameterValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/07eb33be-71a3-42fc-b7f3-12be23746aa3">IAzBizRuleParameters</a>



<a href="https://msdn.microsoft.com/161f8a84-ee00-4f39-9997-a1e3d1c5b7a8">IAzClientContext3::BizRuleParameters</a>
 

 

