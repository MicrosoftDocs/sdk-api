---
UID: NF:sbtsv.ITsSbProvider.CreateTargetObject
title: ITsSbProvider::CreateTargetObject
author: windows-driver-content
description: Creates an ITsSbTarget target object.
old-location: termserv\itssbprovider_createtargetobject.htm
old-project: TermServ
ms.assetid: 9ee426a3-03fa-4535-84b6-f965bd9eba60
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: CreateTargetObject, CreateTargetObject method [Remote Desktop Services], CreateTargetObject method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],CreateTargetObject method, ITsSbProvider.CreateTargetObject, ITsSbProvider::CreateTargetObject, sbtsv/ITsSbProvider::CreateTargetObject, termserv.itssbprovider_createtargetobject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TS_SB_SORT_BY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbtsv.h
api_name:
-	ITsSbProvider.CreateTargetObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITsSbProvider::CreateTargetObject


## -description


Creates an <a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a> target object.


## -parameters




### -param TargetName [in]

A <b>BSTR</b> variable that contains the target name.


### -param EnvironmentName




### -param ppTarget [out]

A pointer to a pointer to the specified target object. When you have finished using the object, release it by calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method.


## -returns



This method can return one of these values.


If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.






## -remarks



Plug-ins can use this method to create a target object.




## -see-also




<a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a>



<a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a>
 

 

