---
UID: NF:azroles.IAzRole.get_ApplicationData
title: IAzRole::get_ApplicationData
author: windows-sdk-content
description: The ApplicationData property of IAzRole sets or retrieves an opaque field that can be used by the application to store information.
old-location: security\iazrole_applicationdata.htm
old-project: SecAuthZ
ms.assetid: 6cb85528-35b4-4fed-98bb-6209dd0af0fd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ApplicationData property [Security], ApplicationData property [Security],AzRole object, ApplicationData property [Security],IAzRole interface, AzRole object [Security],ApplicationData property, IAzRole interface [Security],ApplicationData property, IAzRole.ApplicationData, IAzRole.get_ApplicationData, IAzRole::ApplicationData, IAzRole::get_ApplicationData, IAzRole::put_ApplicationData, azroles/IAzRole::ApplicationData, azroles/IAzRole::get_ApplicationData, azroles/IAzRole::put_ApplicationData, get_ApplicationData, security.iazrole_applicationdata
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
 - IAzRole.ApplicationData
 - IAzRole.get_ApplicationData
 - IAzRole.put_ApplicationData
 - AzRole.ApplicationData
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzRole::get_ApplicationData


## -description


The <b>ApplicationData</b> property sets or retrieves an opaque field that can be used by the application to store information.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Important</b>  Policy administrators can read from and write to this property. Applications should not store data in the <b>ApplicationData</b> property that should not be available to the policy administrator.</div>
<div> </div>


