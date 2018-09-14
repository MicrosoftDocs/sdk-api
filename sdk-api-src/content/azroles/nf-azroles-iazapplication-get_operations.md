---
UID: NF:azroles.IAzApplication.get_Operations
title: IAzApplication::get_Operations
author: windows-sdk-content
description: Retrieves an IAzOperations object that is used to enumerate IAzOperation objects from the policy data.
old-location: security\iazapplication_operations.htm
tech.root: secauthz
ms.assetid: 274a130a-3a3c-46fc-9d2a-3123cdc98d4b
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: AzApplication object [Security],Operations property, IAzApplication interface [Security],Operations property, IAzApplication.Operations, IAzApplication.get_Operations, IAzApplication::Operations, IAzApplication::get_Operations, Operations property [Security], Operations property [Security],AzApplication object, Operations property [Security],IAzApplication interface, azroles/IAzApplication::Operations, azroles/IAzApplication::get_Operations, get_Operations, security.iazapplication_operations
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
 - IAzApplication.Operations
 - IAzApplication.get_Operations
 - AzApplication.Operations
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication::get_Operations


## -description


The <b>Operations</b> property retrieves an <a href="https://msdn.microsoft.com/43db28af-86cb-4530-a87b-d11061533d84">IAzOperations</a> object that is used to enumerate <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> objects from the policy data.

This property is read-only.


## -parameters


## -remarks



This property can be used only to enumerate <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> objects that are direct child objects of the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.



