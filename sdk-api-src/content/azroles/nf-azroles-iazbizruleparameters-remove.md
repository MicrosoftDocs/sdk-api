---
UID: NF:azroles.IAzBizRuleParameters.Remove
title: IAzBizRuleParameters::Remove
author: windows-sdk-content
description: Removes the specified parameter from the list of parameters available to business rule (BizRule) scripts.
old-location: security\iazbizruleparameters_remove_method.htm
tech.root: secauthz
ms.assetid: 1874ac48-0a06-4387-89c2-c194b60bb8f2
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: IAzBizRuleParameters interface [Security],Remove method, IAzBizRuleParameters.Remove, IAzBizRuleParameters::Remove, Remove, Remove method [Security], Remove method [Security],IAzBizRuleParameters interface, azroles/IAzBizRuleParameters::Remove, security.iazbizruleparameters_remove_method
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
 - IAzBizRuleParameters.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- azroles.h
: 
- IAzBizRuleParameters.Remove
: 
---

# IAzBizRuleParameters::Remove


## -description


The <b>Remove</b> method removes the specified parameter from the list of parameters available to business rule (BizRule) scripts.


## -parameters




### -param varParameterName [in]

The name of the parameter to remove.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377646(v=VS.85).aspx">IAzBizRuleParameters</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377876(v=VS.85).aspx">IAzClientContext3::BizRuleParameters</a>
 

 

