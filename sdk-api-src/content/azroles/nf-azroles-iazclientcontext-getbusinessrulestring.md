---
UID: NF:azroles.IAzClientContext.GetBusinessRuleString
title: IAzClientContext::GetBusinessRuleString (azroles.h)
description: Returns the application-specific string for the business rule (BizRule).
helpviewer_keywords: ["AzClientContext object [Security]","GetBusinessRuleString method","GetBusinessRuleString","GetBusinessRuleString method [Security]","GetBusinessRuleString method [Security]","AzClientContext object","GetBusinessRuleString method [Security]","IAzClientContext interface","IAzClientContext interface [Security]","GetBusinessRuleString method","IAzClientContext.GetBusinessRuleString","IAzClientContext::GetBusinessRuleString","azroles/IAzClientContext::GetBusinessRuleString","security.iazclientcontext_getbusinessrulestring"]
old-location: security\iazclientcontext_getbusinessrulestring.htm
tech.root: security
ms.assetid: 44cd9331-4891-45fe-9392-04c19da0ac7d
ms.date: 12/05/2018
ms.keywords: AzClientContext object [Security],GetBusinessRuleString method, GetBusinessRuleString, GetBusinessRuleString method [Security], GetBusinessRuleString method [Security],AzClientContext object, GetBusinessRuleString method [Security],IAzClientContext interface, IAzClientContext interface [Security],GetBusinessRuleString method, IAzClientContext.GetBusinessRuleString, IAzClientContext::GetBusinessRuleString, azroles/IAzClientContext::GetBusinessRuleString, security.iazclientcontext_getbusinessrulestring
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
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzClientContext::GetBusinessRuleString
 - azroles/IAzClientContext::GetBusinessRuleString
dev_langs:
 - c++
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

<a href="/windows/desktop/api/azroles/nf-azroles-iazbizrulecontext-get_businessrulestring">BusinessRuleString</a>



<a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext">IAzClientContext</a>