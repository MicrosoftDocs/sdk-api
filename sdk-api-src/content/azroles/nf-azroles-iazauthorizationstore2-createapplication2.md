---
UID: NF:azroles.IAzAuthorizationStore2.CreateApplication2
title: IAzAuthorizationStore2::CreateApplication2
author: windows-sdk-content
description: Creates an IAzApplication2 object by using the specified name.
old-location: security\iazauthorizationstore2_createapplication2.htm
old-project: secauthz
ms.assetid: d9af40e4-9ed9-4b81-b808-315eef07a96d
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: CreateApplication2, CreateApplication2 method [Security], CreateApplication2 method [Security],IAzAuthorizationStore2 interface, IAzAuthorizationStore2 interface [Security],CreateApplication2 method, IAzAuthorizationStore2.CreateApplication2, IAzAuthorizationStore2::CreateApplication2, azroles/IAzAuthorizationStore2::CreateApplication2, security.iazauthorizationstore2_createapplication2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - IAzAuthorizationStore2.CreateApplication2
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore2::CreateApplication2


## -description


The <b>CreateApplication2</b> method creates an <a href="https://msdn.microsoft.com/58f0627e-fa92-4b3b-a0cd-7e437d451606">IAzApplication2</a> object by using the specified name.


## -parameters




### -param bstrApplicationName [in]

The name for the new <a href="https://msdn.microsoft.com/58f0627e-fa92-4b3b-a0cd-7e437d451606">IAzApplication2</a> object.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppApplication [out]

A pointer to a pointer to the created <a href="https://msdn.microsoft.com/58f0627e-fa92-4b3b-a0cd-7e437d451606">IAzApplication2</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



You must call the <a href="https://msdn.microsoft.com/d00d55a1-884f-46c2-b80b-f90ce8f5c648">IAzApplication::Submit</a> method to persist any changes made by the returned object.

The returned <a href="https://msdn.microsoft.com/58f0627e-fa92-4b3b-a0cd-7e437d451606">IAzApplication2</a> object is an immediate child object of the <a href="https://msdn.microsoft.com/8b3901a9-003f-4346-a0c7-34a1ed730949">IAzAuthorizationStore2</a> object.



