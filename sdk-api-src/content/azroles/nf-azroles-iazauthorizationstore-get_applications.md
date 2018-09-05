---
UID: NF:azroles.IAzAuthorizationStore.get_Applications
title: IAzAuthorizationStore::get_Applications
author: windows-sdk-content
description: Retrieves an IAzApplications object that is used to enumerate IAzApplication objects from the policy store.
old-location: security\azauthorizationstore_applications.htm
old-project: SecAuthZ
ms.assetid: 7475fe41-b2fc-4a2c-a0db-c8c00bcc3ba4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Applications property [Security], Applications property [Security],AzAuthorizationStore object, Applications property [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],Applications property, IAzAuthorizationStore interface [Security],Applications property, IAzAuthorizationStore.Applications, IAzAuthorizationStore.get_Applications, IAzAuthorizationStore::Applications, IAzAuthorizationStore::get_Applications, azroles/IAzAuthorizationStore::Applications, azroles/IAzAuthorizationStore::get_Applications, get_Applications, security.azauthorizationstore_applications
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
 - IAzAuthorizationStore.Applications
 - IAzAuthorizationStore.get_Applications
 - AzAuthorizationStore.Applications
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::get_Applications


## -description


The <b>Applications</b> property retrieves an <a href="https://msdn.microsoft.com/04cee21c-253a-463a-9231-592ddad88188">IAzApplications</a> object that is used to enumerate <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> objects from the policy store.

This property is read-only.


## -parameters


## -remarks



This property can be used only to enumerate <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> objects that are direct child objects of the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object.



