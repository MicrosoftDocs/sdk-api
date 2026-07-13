---
UID: NF:azroles.IAzBizRuleContext.put_BusinessRuleString
title: IAzBizRuleContext::put_BusinessRuleString (azroles.h)
description: Sets or retrieves an application-specific string for the Business Rule (BizRule). (Put)
helpviewer_keywords: ["AzBizRuleContext object [Security]","BusinessRuleString property","BusinessRuleString property [Security]","BusinessRuleString property [Security]","AzBizRuleContext object","BusinessRuleString property [Security]","IAzBizRuleContext interface","IAzBizRuleContext interface [Security]","BusinessRuleString property","IAzBizRuleContext.BusinessRuleString","IAzBizRuleContext.put_BusinessRuleString","IAzBizRuleContext::BusinessRuleString","IAzBizRuleContext::get_BusinessRuleString","IAzBizRuleContext::put_BusinessRuleString","azroles/IAzBizRuleContext::BusinessRuleString","azroles/IAzBizRuleContext::get_BusinessRuleString","azroles/IAzBizRuleContext::put_BusinessRuleString","put_BusinessRuleString","security.azbizrulecontext_businessrulestring"]
old-location: security\azbizrulecontext_businessrulestring.htm
tech.root: security
ms.assetid: 0370b251-625a-410c-ab36-76f4432405cf
ms.date: 12/05/2018
ms.keywords: AzBizRuleContext object [Security],BusinessRuleString property, BusinessRuleString property [Security], BusinessRuleString property [Security],AzBizRuleContext object, BusinessRuleString property [Security],IAzBizRuleContext interface, IAzBizRuleContext interface [Security],BusinessRuleString property, IAzBizRuleContext.BusinessRuleString, IAzBizRuleContext.put_BusinessRuleString, IAzBizRuleContext::BusinessRuleString, IAzBizRuleContext::get_BusinessRuleString, IAzBizRuleContext::put_BusinessRuleString, azroles/IAzBizRuleContext::BusinessRuleString, azroles/IAzBizRuleContext::get_BusinessRuleString, azroles/IAzBizRuleContext::put_BusinessRuleString, put_BusinessRuleString, security.azbizrulecontext_businessrulestring
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
 - IAzBizRuleContext::put_BusinessRuleString
 - azroles/IAzBizRuleContext::put_BusinessRuleString
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
 - IAzBizRuleContext.BusinessRuleString
 - IAzBizRuleContext.get_BusinessRuleString
 - IAzBizRuleContext.put_BusinessRuleString
 - AzBizRuleContext.BusinessRuleString
---

# IAzBizRuleContext::put_BusinessRuleString


## -description

The <b>BusinessRuleString</b> property sets or retrieves an application-specific string for the Business Rule (BizRule).

This property is read/write.

## -parameters

## -remarks

This property is returned to the application that called the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">IAzClientContext::AccessCheck</a> method. One possible use of this property is to explain the reason that the BizRule denied access to the user.

The maximum length of this property is 65,536 characters.
