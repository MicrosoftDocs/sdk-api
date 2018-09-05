---
UID: NF:azroles.IAzTask.put_BizRuleImportedPath
title: IAzTask::put_BizRuleImportedPath
author: windows-sdk-content
description: Sets or retrieves the path to the file from which the business rule (BizRule) is imported.
old-location: security\iaztask_bizruleimportedpath.htm
old-project: SecAuthZ
ms.assetid: 52422e14-4a96-455d-ad35-b8816871ee10
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AzTask object [Security],BizRuleImportedPath property, BizRuleImportedPath property [Security], BizRuleImportedPath property [Security],AzTask object, BizRuleImportedPath property [Security],IAzTask interface, IAzTask interface [Security],BizRuleImportedPath property, IAzTask.BizRuleImportedPath, IAzTask.put_BizRuleImportedPath, IAzTask::BizRuleImportedPath, IAzTask::get_BizRuleImportedPath, IAzTask::put_BizRuleImportedPath, azroles/IAzTask::BizRuleImportedPath, azroles/IAzTask::get_BizRuleImportedPath, azroles/IAzTask::put_BizRuleImportedPath, put_BizRuleImportedPath, security.iaztask_bizruleimportedpath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
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
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
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




<a href="https://msdn.microsoft.com/cf3d87af-5320-4fe0-b513-e242f8a1dd1b">BizRule</a>



<a href="https://msdn.microsoft.com/922f4fd8-f553-439c-b9ae-51a45a88adc7">BizRuleLanguage</a>



<a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a>
 

 

