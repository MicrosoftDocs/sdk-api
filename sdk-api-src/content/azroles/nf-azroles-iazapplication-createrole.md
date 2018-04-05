---
UID: NF:azroles.IAzApplication.CreateRole
title: IAzApplication::CreateRole method
author: windows-driver-content
description: Creates an IAzRole object with the specified name.
old-location: security\iazapplication_createrole.htm
old-project: SecAuthZ
ms.assetid: abad30e8-a483-4c29-ae87-4218882e8319
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: AzApplication object [Security], CreateRole method, CreateRole method [Security], CreateRole method [Security], AzApplication object, CreateRole method [Security], IAzApplication interface, CreateRole,IAzApplication.CreateRole, IAzApplication, IAzApplication interface [Security], CreateRole method, IAzApplication::CreateRole, azroles/IAzApplication::CreateRole, security.iazapplication_createrole
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
-	IAzApplication.CreateRole
-	AzApplication.CreateRole
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::CreateRole method


## -description


The <b>CreateRole</b> method creates an <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object with the specified name.


## -parameters




### -param bstrRoleName [in]

Name for the new <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppRole [out]

A pointer to a pointer to the created <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/97f2018a-92f0-4ebb-85f1-78c140003d8f">IAzRole::Submit</a> method to persist any changes made to the returned object.

The returned <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object is an immediate child object of the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.



