---
UID: NF:azroles.IAzTask.get_BizRule
title: IAzTask::get_BizRule (azroles.h)
description: Sets or retrieves the text of the script that implements the business rule (BizRule). (Get)
helpviewer_keywords: ["AzTask object [Security]","BizRule property","BizRule property [Security]","BizRule property [Security]","AzTask object","BizRule property [Security]","IAzTask interface","IAzTask interface [Security]","BizRule property","IAzTask.BizRule","IAzTask.get_BizRule","IAzTask::BizRule","IAzTask::get_BizRule","IAzTask::put_BizRule","azroles/IAzTask::BizRule","azroles/IAzTask::get_BizRule","azroles/IAzTask::put_BizRule","get_BizRule","security.iaztask_bizrule"]
old-location: security\iaztask_bizrule.htm
tech.root: security
ms.assetid: cf3d87af-5320-4fe0-b513-e242f8a1dd1b
ms.date: 12/05/2018
ms.keywords: AzTask object [Security],BizRule property, BizRule property [Security], BizRule property [Security],AzTask object, BizRule property [Security],IAzTask interface, IAzTask interface [Security],BizRule property, IAzTask.BizRule, IAzTask.get_BizRule, IAzTask::BizRule, IAzTask::get_BizRule, IAzTask::put_BizRule, azroles/IAzTask::BizRule, azroles/IAzTask::get_BizRule, azroles/IAzTask::put_BizRule, get_BizRule, security.iaztask_bizrule
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
 - IAzTask::get_BizRule
 - azroles/IAzTask::get_BizRule
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
 - IAzTask.BizRule
 - IAzTask.get_BizRule
 - IAzTask.put_BizRule
 - AzTask.BizRule
---

# IAzTask::get_BizRule


## -description

The <b>BizRule</b> property sets or retrieves the text of the script that implements the business rule (BizRule).

This property is read/write.

## -parameters

## -remarks

The maximum length of this property is 65,536 characters.

<div class="alert"><b>Important</b>  The <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_bizrulelanguage">BizRuleLanguage</a> property must be set before this property is set.</div>
<div> </div>
An <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object that is a child object of a delegated <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object cannot have an associated BizRule.

## -see-also

<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_bizruleimportedpath">BizRuleImportedPath</a>



<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_bizrulelanguage">BizRuleLanguage</a>



<a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a>
