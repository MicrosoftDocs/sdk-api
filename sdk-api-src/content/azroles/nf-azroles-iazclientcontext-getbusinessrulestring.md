---
UID: NF:azroles.IAzClientContext.GetBusinessRuleString
title: IAzClientContext::GetBusinessRuleString
author: windows-sdk-content
description: Returns the application-specific string for the business rule (BizRule).
old-location: security\iazclientcontext_getbusinessrulestring.htm
tech.root: SecAuthZ
ms.assetid: 44cd9331-4891-45fe-9392-04c19da0ac7d
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: AzClientContext object [Security],GetBusinessRuleString method, GetBusinessRuleString, GetBusinessRuleString method [Security], GetBusinessRuleString method [Security],AzClientContext object, GetBusinessRuleString method [Security],IAzClientContext interface, IAzClientContext interface [Security],GetBusinessRuleString method, IAzClientContext.GetBusinessRuleString, IAzClientContext::GetBusinessRuleString, azroles/IAzClientContext::GetBusinessRuleString, security.iazclientcontext_getbusinessrulestring
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAzClientContext.GetBusinessRuleString
 - AzClientContext.GetBusinessRuleString
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzClientContext::GetBusinessRuleString


## -description


The <b>GetBusinessRuleString</b> method returns the application-specific string for the business rule (BizRule).


## -parameters




### -param pbstrBusinessRuleString [out]

String that contains information about the BizRule. The  format and contents of the string are  defined by the application.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.




## -see-also




<a href="https://msdn.microsoft.com/0370b251-625a-410c-ab36-76f4432405cf">BusinessRuleString</a>



<a href="https://msdn.microsoft.com/e24184d2-a77b-4a8b-b2f3-78f1e0b902f9">IAzClientContext</a>
 

 

