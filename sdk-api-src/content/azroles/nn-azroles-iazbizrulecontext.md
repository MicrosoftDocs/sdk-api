---
UID: NN:azroles.IAzBizRuleContext
title: IAzBizRuleContext (azroles.h)
description: Contains information about a Business Rule (BizRule) operation.
helpviewer_keywords: ["IAzBizRuleContext","IAzBizRuleContext interface [Security]","IAzBizRuleContext interface [Security]","described","azroles/IAzBizRuleContext","security.azbizrulecontext"]
old-location: security\azbizrulecontext.htm
tech.root: security
ms.assetid: 664d0307-8915-4435-a6a3-3f464afd9029
ms.date: 12/05/2018
ms.keywords: IAzBizRuleContext, IAzBizRuleContext interface [Security], IAzBizRuleContext interface [Security],described, azroles/IAzBizRuleContext, security.azbizrulecontext
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
 - IAzBizRuleContext
 - azroles/IAzBizRuleContext
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
 - IAzBizRuleContext
---

# IAzBizRuleContext interface


## -description

The <b>AzBizRuleContext</b> object contains information about a Business Rule (BizRule) operation.

## -inheritance

The <b>IAzBizRuleContext</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAzBizRuleContext</b> also has these types of members:

## -remarks

The <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">IAzClientContext::AccessCheck</a> method creates an <b>AzBizRuleContext</b> object before it calls a BizRule script.
