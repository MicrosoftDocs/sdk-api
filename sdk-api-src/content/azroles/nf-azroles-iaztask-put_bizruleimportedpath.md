---
UID: NF:azroles.IAzTask.put_BizRuleImportedPath
title: IAzTask::put_BizRuleImportedPath (azroles.h)
description: Sets or retrieves the path to the file from which the business rule (BizRule) is imported. (Put)
helpviewer_keywords: ["AzTask object [Security]","BizRuleImportedPath property","BizRuleImportedPath property [Security]","BizRuleImportedPath property [Security]","AzTask object","BizRuleImportedPath property [Security]","IAzTask interface","IAzTask interface [Security]","BizRuleImportedPath property","IAzTask.BizRuleImportedPath","IAzTask.put_BizRuleImportedPath","IAzTask::BizRuleImportedPath","IAzTask::get_BizRuleImportedPath","IAzTask::put_BizRuleImportedPath","azroles/IAzTask::BizRuleImportedPath","azroles/IAzTask::get_BizRuleImportedPath","azroles/IAzTask::put_BizRuleImportedPath","put_BizRuleImportedPath","security.iaztask_bizruleimportedpath"]
old-location: security\iaztask_bizruleimportedpath.htm
tech.root: security
ms.assetid: 52422e14-4a96-455d-ad35-b8816871ee10
ms.date: 12/05/2018
ms.keywords: AzTask object [Security],BizRuleImportedPath property, BizRuleImportedPath property [Security], BizRuleImportedPath property [Security],AzTask object, BizRuleImportedPath property [Security],IAzTask interface, IAzTask interface [Security],BizRuleImportedPath property, IAzTask.BizRuleImportedPath, IAzTask.put_BizRuleImportedPath, IAzTask::BizRuleImportedPath, IAzTask::get_BizRuleImportedPath, IAzTask::put_BizRuleImportedPath, azroles/IAzTask::BizRuleImportedPath, azroles/IAzTask::get_BizRuleImportedPath, azroles/IAzTask::put_BizRuleImportedPath, put_BizRuleImportedPath, security.iaztask_bizruleimportedpath
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
 - IAzTask::put_BizRuleImportedPath
 - azroles/IAzTask::put_BizRuleImportedPath
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
 - IAzTask.BizRuleImportedPath
 - IAzTask.get_BizRuleImportedPath
 - IAzTask.put_BizRuleImportedPath
 - AzTask.BizRuleImportedPath
---

# IAzTask::put_BizRuleImportedPath


## -description

The <b>BizRuleImportedPath</b> property sets or retrieves the path to the file from which the business rule (BizRule) is imported.

This property is read/write.

## -parameters

## -remarks

The path information is stored for use by the UI. The UI should supply a mechanism to synchronize the contents of the file and this property.

The maximum length of this property is 512 characters.

## -see-also

<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_bizrule">BizRule</a>



<a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_bizrulelanguage">BizRuleLanguage</a>



<a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a>
