---
UID: NF:azroles.IAzBizRuleParameters.Remove
title: IAzBizRuleParameters::Remove method
author: windows-driver-content
description: Removes the specified parameter from the list of parameters available to business rule (BizRule) scripts.
old-location: security\iazbizruleparameters_remove_method.htm
old-project: SecAuthZ
ms.assetid: 1874ac48-0a06-4387-89c2-c194b60bb8f2
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IAzBizRuleParameters, IAzBizRuleParameters interface [Security], Remove method, IAzBizRuleParameters::Remove, Remove method [Security], Remove method [Security], IAzBizRuleParameters interface, Remove,IAzBizRuleParameters.Remove, azroles/IAzBizRuleParameters::Remove, security.iazbizruleparameters_remove_method
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.h
api_name:
-	IAzBizRuleParameters.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAzBizRuleParameters::Remove method


## -description


The <b>Remove</b> method removes the specified parameter from the list of parameters available to business rule (BizRule) scripts.


## -parameters




### -param varParameterName [in]

The name of the parameter to remove.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/07eb33be-71a3-42fc-b7f3-12be23746aa3">IAzBizRuleParameters</a>



<a href="https://msdn.microsoft.com/161f8a84-ee00-4f39-9997-a1e3d1c5b7a8">IAzClientContext3::BizRuleParameters</a>
 

 

