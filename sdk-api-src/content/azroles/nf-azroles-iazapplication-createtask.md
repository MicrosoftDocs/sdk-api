---
UID: NF:azroles.IAzApplication.CreateTask
title: IAzApplication::CreateTask
author: windows-sdk-content
description: Creates an IAzTask object with the specified name.
old-location: security\iazapplication_createtask.htm
tech.root: secauthz
ms.assetid: 9c15f1aa-f0d7-4c6b-8c3c-b6537f7dac90
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: AzApplication object [Security],CreateTask method, CreateTask, CreateTask method [Security], CreateTask method [Security],AzApplication object, CreateTask method [Security],IAzApplication interface, IAzApplication interface [Security],CreateTask method, IAzApplication.CreateTask, IAzApplication::CreateTask, azroles/IAzApplication::CreateTask, security.iazapplication_createtask
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
 - IAzApplication.CreateTask
 - AzApplication.CreateTask
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication::CreateTask


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



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/a6f01573-c1ee-421d-8591-e1c9fa6c3d68">IAzTask::Submit</a> method to persist any changes made to the returned object.

The returned <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object is an immediate child object of the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.



