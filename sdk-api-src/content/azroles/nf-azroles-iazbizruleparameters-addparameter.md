---
UID: NF:azroles.IAzBizRuleParameters.AddParameter
title: IAzBizRuleParameters::AddParameter
author: windows-sdk-content
description: Adds a parameter to the list of parameters available to business rule (BizRule) scripts.
old-location: security\iazbizruleparameters_addparameter_method.htm
old-project: secauthz
ms.assetid: ea5c45d4-34c8-4d7c-a1b2-8f45574d9449
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: AddParameter, AddParameter method [Security], AddParameter method [Security],IAzBizRuleParameters interface, IAzBizRuleParameters interface [Security],AddParameter method, IAzBizRuleParameters.AddParameter, IAzBizRuleParameters::AddParameter, azroles/IAzBizRuleParameters::AddParameter, security.iazbizruleparameters_addparameter_method
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzBizRuleParameters.AddParameter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/07eb33be-71a3-42fc-b7f3-12be23746aa3">IAzBizRuleParameters</a>



<a href="https://msdn.microsoft.com/161f8a84-ee00-4f39-9997-a1e3d1c5b7a8">IAzClientContext3::BizRuleParameters</a>
 

 

