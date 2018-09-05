---
UID: NF:azroles.IAzApplication.CreateApplicationGroup
title: IAzApplication::CreateApplicationGroup
author: windows-sdk-content
description: Creates an IAzApplicationGroup object with the specified name.
old-location: security\iazapplication_createapplicationgroup.htm
old-project: SecAuthZ
ms.assetid: 86f1694e-09a4-4a53-ae63-cfdb5d2e44ed
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AzApplication object [Security],CreateApplicationGroup method, CreateApplicationGroup, CreateApplicationGroup method [Security], CreateApplicationGroup method [Security],AzApplication object, CreateApplicationGroup method [Security],IAzApplication interface, IAzApplication interface [Security],CreateApplicationGroup method, IAzApplication.CreateApplicationGroup, IAzApplication::CreateApplicationGroup, azroles/IAzApplication::CreateApplicationGroup, security.iazapplication_createapplicationgroup
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
 - IAzApplication.CreateApplicationGroup
 - AzApplication.CreateApplicationGroup
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::CreateApplicationGroup


## -description


The <b>CreateApplicationGroup</b> method creates an <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object with the specified name.


## -parameters




### -param bstrGroupName [in]

Name for the new <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppGroup [out]

A pointer to a pointer to the created <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/51a855dd-4a90-4f7a-b32f-f91e3941655b">IAzApplicationGroup::Submit</a> method to persist any changes made to the returned object.

The returned <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object is an immediate child object of the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.



