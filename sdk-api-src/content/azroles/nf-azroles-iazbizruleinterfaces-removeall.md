---
UID: NF:azroles.IAzBizRuleInterfaces.RemoveAll
title: IAzBizRuleInterfaces::RemoveAll (azroles.h)
description: Removes all interfaces from the list of interfaces that can be called by business rule (BizRule) scripts.
helpviewer_keywords: ["IAzBizRuleInterfaces interface [Security]","RemoveAll method","IAzBizRuleInterfaces.RemoveAll","IAzBizRuleInterfaces::RemoveAll","RemoveAll","RemoveAll method [Security]","RemoveAll method [Security]","IAzBizRuleInterfaces interface","azroles/IAzBizRuleInterfaces::RemoveAll","security.iazbizruleinterfaces_removeall_method"]
old-location: security\iazbizruleinterfaces_removeall_method.htm
tech.root: security
ms.assetid: 05e0d7af-5b09-4112-9229-862197a9895b
ms.date: 03/20/2023
ms.keywords: IAzBizRuleInterfaces interface [Security],RemoveAll method, IAzBizRuleInterfaces.RemoveAll, IAzBizRuleInterfaces::RemoveAll, RemoveAll, RemoveAll method [Security], RemoveAll method [Security],IAzBizRuleInterfaces interface, azroles/IAzBizRuleInterfaces::RemoveAll, security.iazbizruleinterfaces_removeall_method
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzBizRuleInterfaces::RemoveAll
 - azroles/IAzBizRuleInterfaces::RemoveAll
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzBizRuleInterfaces.RemoveAll
---

# IAzBizRuleInterfaces::RemoveAll

## -description

The **RemoveAll** method removes all interfaces from the list of interfaces that can be called by business rule (BizRule) scripts.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -see-also

[AddInterface](nf-azroles-iazbizruleinterfaces-addinterface.md)

[IAzBizRuleInterfaces](nn-azroles-iazbizruleinterfaces.md)
