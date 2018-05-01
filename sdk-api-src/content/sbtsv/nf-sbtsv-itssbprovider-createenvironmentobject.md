---
UID: NF:sbtsv.ITsSbProvider.CreateEnvironmentObject
title: ITsSbProvider::CreateEnvironmentObject method
author: windows-driver-content
description: Creates an ITsSbEnvironment environment object.
old-location: termserv\itssbprovider_createenvironmentobject.htm
old-project: TermServ
ms.assetid: 11570f40-979e-4caf-81af-f8d16ec61391
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: CreateEnvironmentObject method [Remote Desktop Services], CreateEnvironmentObject method [Remote Desktop Services], ITsSbProvider interface, CreateEnvironmentObject,ITsSbProvider.CreateEnvironmentObject, ITsSbProvider, ITsSbProvider interface [Remote Desktop Services], CreateEnvironmentObject method, ITsSbProvider::CreateEnvironmentObject, sbtsv/ITsSbProvider::CreateEnvironmentObject, termserv.itssbprovider_createenvironmentobject
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
-	ITsSbProvider.CreateEnvironmentObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITsSbProvider::CreateEnvironmentObject method


## -description


Creates an <a href="https://msdn.microsoft.com/287cea18-c13c-4396-8970-39dd7f9b960e">ITsSbEnvironment</a> environment object.


## -parameters




### -param Name [in]

A <b>BSTR</b> variable that contains the name of the object to create.


### -param ServerWeight [in]

A <b>DWORD</b> variable that contains the server weight of the object to create.


### -param ppEnvironment [out]

A pointer to a pointer to the newly created environment object. When you have finished using the object, release it by calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method.


## -returns



This method can return one of these values.


If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.






## -remarks



Plug-ins can use this method to create an environment object.




## -see-also




<a href="https://msdn.microsoft.com/287cea18-c13c-4396-8970-39dd7f9b960e">ITsSbEnvironment</a>



<a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a>
 

 

