---
UID: NF:comsvcs.ObjectContext.get_Security
title: ObjectContext::get_Security
author: windows-sdk-content
description: Retrieves the security object of the current object's context.
old-location: cos\objectcontext_get_security.htm
old-project: cossdk
ms.assetid: a160d214-b807-47cd-a712-b4cad941a157
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ObjectContext interface [COM+],get_Security method, ObjectContext.get_Security, ObjectContext::get_Security, _cos_ObjectContext_get_Security, comsvcs/ObjectContext::get_Security, cos.objectcontext_get_security, get_Security, get_Security method [COM+], get_Security method [COM+],ObjectContext interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ObjectContext.get_Security
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ObjectContext::get_Security


## -description


Retrieves the security object of the current object's context.


## -parameters




### -param ppSecurityProperty [out]

A reference to a <a href="https://msdn.microsoft.com/e4eb8e83-3510-4c2c-8b9c-563bfcbf48b3">SecurityProperty</a> interface that contains the security property of the current object's context.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/09a17e57-7224-43bc-93c7-16ab95ca2517">ObjectContext</a>
 

 

