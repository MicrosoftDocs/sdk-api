---
UID: NF:azroles.IAzRole.AddTask
title: IAzRole::AddTask
author: windows-driver-content
description: Adds the IAzTask object with the specified name to the role.
old-location: security\iazrole_addtask.htm
old-project: SecAuthZ
ms.assetid: 51ba30c3-8067-4aca-b8aa-8e64d4427b98
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: AddTask, AddTask method [Security], AddTask method [Security],AzRole object, AddTask method [Security],IAzRole interface, AzRole object [Security],AddTask method, IAzRole interface [Security],AddTask method, IAzRole.AddTask, IAzRole::AddTask, azroles/IAzRole::AddTask, security.iazrole_addtask
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
-	IAzRole.AddTask
-	AzRole.AddTask
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzRole::AddTask


## -description


The <b>AddTask</b> method adds the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object with the specified name to the role.


## -parameters




### -param bstrProp [in]

Name of the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object to add to the role.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



You must call the <a href="https://msdn.microsoft.com/97f2018a-92f0-4ebb-85f1-78c140003d8f">Submit</a> method to persist any changes made by this method.



