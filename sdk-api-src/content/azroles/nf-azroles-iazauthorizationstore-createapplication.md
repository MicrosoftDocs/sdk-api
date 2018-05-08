---
UID: NF:azroles.IAzAuthorizationStore.CreateApplication
title: IAzAuthorizationStore::CreateApplication
author: windows-driver-content
description: Creates an IAzApplication object with the specified name.
old-location: security\azauthorizationstore_createapplication.htm
old-project: SecAuthZ
ms.assetid: ca6feb69-15cd-454a-a2b8-c75c4c6b38cd
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AzAuthorizationStore object [Security],CreateApplication method, CreateApplication, CreateApplication method [Security], CreateApplication method [Security],AzAuthorizationStore object, CreateApplication method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],CreateApplication method, IAzAuthorizationStore.CreateApplication, IAzAuthorizationStore::CreateApplication, azroles/IAzAuthorizationStore::CreateApplication, security.azauthorizationstore_createapplication
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
-	AzAuthorizationStore.CreateApplication
-	IAzAuthorizationStore.CreateApplication
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::CreateApplication


## -description


The <b>CreateApplication</b> method creates an <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object with the specified name.


## -parameters




### -param bstrApplicationName [in]

Name for the new <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppApplication [out]

A pointer to a pointer to the created <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/d00d55a1-884f-46c2-b80b-f90ce8f5c648">IAzApplication::Submit</a> method to persist any changes made by the returned object.

The returned <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object is an immediate child object of the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object.



