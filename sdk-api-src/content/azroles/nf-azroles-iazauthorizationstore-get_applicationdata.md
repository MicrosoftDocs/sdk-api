---
UID: NF:azroles.IAzAuthorizationStore.get_ApplicationData
title: IAzAuthorizationStore::get_ApplicationData
author: windows-sdk-content
description: Sets or retrieves an opaque field that can be used by the application to store information.
old-location: security\azauthorizationstore_applicationdata.htm
old-project: SecAuthZ
ms.assetid: 21a76185-6bcf-405a-a2c5-5509b51ed16e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ApplicationData property [Security], ApplicationData property [Security],AzAuthorizationStore object, ApplicationData property [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],ApplicationData property, IAzAuthorizationStore interface [Security],ApplicationData property, IAzAuthorizationStore.ApplicationData, IAzAuthorizationStore.get_ApplicationData, IAzAuthorizationStore::ApplicationData, IAzAuthorizationStore::get_ApplicationData, IAzAuthorizationStore::put_ApplicationData, azroles/IAzAuthorizationStore::ApplicationData, azroles/IAzAuthorizationStore::get_ApplicationData, azroles/IAzAuthorizationStore::put_ApplicationData, get_ApplicationData, security.azadminmanager_applicationdata, security.azauthorizationstore_applicationdata
ms.prod: windows
ms.technology: windows-sdk
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
 - IAzAuthorizationStore.ApplicationData
 - IAzAuthorizationStore.get_ApplicationData
 - IAzAuthorizationStore.put_ApplicationData
 - AzAuthorizationStore.ApplicationData
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::get_ApplicationData


## -description


The <b>ApplicationData</b> property sets or retrieves an opaque field that can be used by the application to store information.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Important</b>  Policy administrators can read from and write to this property. Applications should not store data in the <b>ApplicationData</b> property that should not be available to the policy administrator.</div>
<div> </div>


