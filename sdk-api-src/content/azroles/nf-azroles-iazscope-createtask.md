---
UID: NF:azroles.IAzScope.CreateTask
title: IAzScope::CreateTask
author: windows-sdk-content
description: Creates an IAzTask object with the specified name.
old-location: security\iazscope_createtask.htm
tech.root: secauthz
ms.assetid: 2be1afd7-8d10-4783-a5ea-3e8c0b103ceb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AzScope object [Security],CreateTask method, CreateTask, CreateTask method [Security], CreateTask method [Security],AzScope object, CreateTask method [Security],IAzScope interface, IAzScope interface [Security],CreateTask method, IAzScope.CreateTask, IAzScope::CreateTask, azroles/IAzScope::CreateTask, security.iazscope_createtask
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzScope.CreateTask
 - AzScope.CreateTask
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzScope::CreateTask


## -description


The <b>CreateTask</b> method creates an <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object with the specified name.


## -parameters




### -param bstrTaskName [in]

Name for the new <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppTask [out]

A pointer to a pointer to the created <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/a6f01573-c1ee-421d-8591-e1c9fa6c3d68">IAzTask::Submit</a> method to persist any changes made to the returned object.

The returned <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object is an immediate child object of the <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object.



