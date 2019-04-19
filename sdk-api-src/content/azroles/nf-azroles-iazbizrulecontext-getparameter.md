---
UID: NF:azroles.IAzBizRuleContext.GetParameter
title: IAzBizRuleContext::GetParameter (azroles.h)
author: windows-sdk-content
description: Gets the specified value from the varParameterValues parameter of the IAzClientContext::AccessCheck method.
old-location: security\azbizrulecontext_getparameter.htm
tech.root: SecAuthZ
ms.assetid: 9c956eea-92a5-4da8-abe0-a5ab4e41ab85
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AzBizRuleContext object [Security],GetParameter method, GetParameter, GetParameter method [Security], GetParameter method [Security],AzBizRuleContext object, GetParameter method [Security],IAzBizRuleContext interface, IAzBizRuleContext interface [Security],GetParameter method, IAzBizRuleContext.GetParameter, IAzBizRuleContext::GetParameter, azroles/IAzBizRuleContext::GetParameter, security.azbizrulecontext_getparameter
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzBizRuleContext.GetParameter
 - AzBizRuleContext.GetParameter
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzBizRuleContext::GetParameter


## -description


The <b>GetParameter</b> method gets the specified value from the <i>varParameterValues</i> parameter of the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">IAzClientContext::AccessCheck</a> method.


## -parameters




### -param bstrParameterName [in]

Name of the value to return. The name must match the name in one of the elements in the array passed into the <i>varParameterNames</i> parameter of the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method. 

<div class="alert"><b>Important</b>  Users of VBScript must be aware that the comparison between this parameter and the names in the <i>varParameterNames</i> parameter is case sensitive.</div>
<div> </div>

### -param pvarParameterValue [out]

Parameter value from the <i>varParameterValues</i> parameter of the <a href="https://msdn.microsoft.com/0bd16cdb-3dba-4656-b264-32e622732155">AccessCheck</a> method that corresponds to the name specified by the <i>bstrParameterName</i> parameter, if found; otherwise, <b>NULL</b>.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.



