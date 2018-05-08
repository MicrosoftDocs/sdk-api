---
UID: NF:azroles.IAzRole.AddOperation
title: IAzRole::AddOperation
author: windows-driver-content
description: Adds the IAzOperation object with the specified name to the role.
old-location: security\iazrole_addoperation.htm
old-project: SecAuthZ
ms.assetid: 8c6d26ff-3287-4a1d-91cb-759f79ec92e5
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AddOperation, AddOperation method [Security], AddOperation method [Security],AzRole object, AddOperation method [Security],IAzRole interface, AzRole object [Security],AddOperation method, IAzRole interface [Security],AddOperation method, IAzRole.AddOperation, IAzRole::AddOperation, azroles/IAzRole::AddOperation, security.iazrole_addoperation
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
-	IAzRole.AddOperation
-	AzRole.AddOperation
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzRole::AddOperation


## -description


The <b>AddOperation</b> method adds the <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object with the specified name to the role.


## -parameters




### -param bstrProp [in]

Name of the <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object to add to the role.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



You must call the <a href="https://msdn.microsoft.com/97f2018a-92f0-4ebb-85f1-78c140003d8f">Submit</a> method to persist any changes made by this method.



