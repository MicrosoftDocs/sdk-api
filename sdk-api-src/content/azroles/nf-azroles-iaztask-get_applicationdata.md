---
UID: NF:azroles.IAzTask.get_ApplicationData
title: IAzTask::get_ApplicationData (azroles.h)
author: windows-sdk-content
description: The ApplicationData property of IAzTask sets or retrieves an opaque field that can be used by the application to store information.
old-location: security\iaztask_applicationdata.htm
tech.root: SecAuthZ
ms.assetid: 0a3939ee-6449-4eef-bb23-11e6d7018f04
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ApplicationData property [Security], ApplicationData property [Security],AzTask object, ApplicationData property [Security],IAzTask interface, AzTask object [Security],ApplicationData property, IAzTask interface [Security],ApplicationData property, IAzTask.ApplicationData, IAzTask.get_ApplicationData, IAzTask::ApplicationData, IAzTask::get_ApplicationData, IAzTask::put_ApplicationData, azroles/IAzTask::ApplicationData, azroles/IAzTask::get_ApplicationData, azroles/IAzTask::put_ApplicationData, get_ApplicationData, security.iaztask_applicationdata
ms.topic: method
f1_keywords: ["azroles/IAzTask.ApplicationData"]
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
 - IAzTask.ApplicationData
 - IAzTask.get_ApplicationData
 - IAzTask.put_ApplicationData
 - AzTask.ApplicationData
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzTask::get_ApplicationData


## -description


The <b>ApplicationData</b> property sets or retrieves an opaque field that can be used by the application to store information.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Important</b>  Policy administrators can read from and write to this property. Applications should not store data in the <b>ApplicationData</b> property that should not be available to the policy administrator.</div>
<div> </div>


