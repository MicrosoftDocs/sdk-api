---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

