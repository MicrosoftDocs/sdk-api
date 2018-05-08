---
UID: NF:azroles.IAzTask.put_BizRule
title: IAzTask::put_BizRule
author: windows-driver-content
description: Sets or retrieves the text of the script that implements the business rule (BizRule).
old-location: security\iaztask_bizrule.htm
old-project: SecAuthZ
ms.assetid: cf3d87af-5320-4fe0-b513-e242f8a1dd1b
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AzTask object [Security],BizRule property, BizRule property [Security], BizRule property [Security],AzTask object, BizRule property [Security],IAzTask interface, IAzTask interface [Security],BizRule property, IAzTask.BizRule, IAzTask.put_BizRule, IAzTask::BizRule, IAzTask::get_BizRule, IAzTask::put_BizRule, azroles/IAzTask::BizRule, azroles/IAzTask::get_BizRule, azroles/IAzTask::put_BizRule, put_BizRule, security.iaztask_bizrule
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzTask.BizRule
-	IAzTask.get_BizRule
-	IAzTask.put_BizRule
-	AzTask.BizRule
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzTask::put_BizRule


## -description


The <b>BizRule</b> property sets or retrieves the text of the script that implements the business rule (BizRule).

This property is read/write.


## -parameters


## -remarks



The maximum length of this property is 65,536 characters.

<div class="alert"><b>Important</b>  The <a href="https://msdn.microsoft.com/922f4fd8-f553-439c-b9ae-51a45a88adc7">BizRuleLanguage</a> property must be set before this property is set.</div>
<div> </div>
An <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object that is a child object of a delegated <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object cannot have an associated BizRule.




## -see-also




<a href="https://msdn.microsoft.com/52422e14-4a96-455d-ad35-b8816871ee10">BizRuleImportedPath</a>



<a href="https://msdn.microsoft.com/922f4fd8-f553-439c-b9ae-51a45a88adc7">BizRuleLanguage</a>



<a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a>
 

 

