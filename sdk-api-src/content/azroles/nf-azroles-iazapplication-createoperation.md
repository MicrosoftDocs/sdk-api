---
UID: NF:azroles.IAzApplication.CreateOperation
title: IAzApplication::CreateOperation
author: windows-sdk-content
description: Creates an IAzOperation object with the specified name.
old-location: security\iazapplication_createoperation.htm
tech.root: SecAuthZ
ms.assetid: 4faf4fc3-5847-40a1-9f85-fb10bb3048b4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AzApplication object [Security],CreateOperation method, CreateOperation, CreateOperation method [Security], CreateOperation method [Security],AzApplication object, CreateOperation method [Security],IAzApplication interface, IAzApplication interface [Security],CreateOperation method, IAzApplication.CreateOperation, IAzApplication::CreateOperation, azroles/IAzApplication::CreateOperation, security.iazapplication_createoperation
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
 - IAzApplication.CreateOperation
 - AzApplication.CreateOperation
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication::CreateOperation


## -description


The <b>CreateOperation</b> method creates an <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object with the specified name.


## -parameters




### -param bstrOperationName [in]

Name for the new <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppOperation [out]

A pointer to a pointer to the created <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/f6265bfa-c856-47db-a688-f5de25ef7157">IAzOperation::Submit</a> method to persist any changes made to the returned object.

The returned <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object is an immediate child object of the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.



