---
UID: NF:sbtsv.ITsSbProvider.CreateSessionObject
title: ITsSbProvider::CreateSessionObject
author: windows-driver-content
description: Plug-ins can use the CreateSessionObject method to create an ITsSbSession session object.
old-location: termserv\itssbprovider_createsessionobject.htm
old-project: TermServ
ms.assetid: 14c800f8-a3d6-4d12-b568-94ef2d8e0aaf
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: CreateSessionObject, CreateSessionObject method [Remote Desktop Services], CreateSessionObject method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],CreateSessionObject method, ITsSbProvider.CreateSessionObject, ITsSbProvider::CreateSessionObject, sbtsv/ITsSbProvider::CreateSessionObject, termserv.itssbprovider_createsessionobject
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
-	ITsSbProvider.CreateSessionObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITsSbProvider::CreateSessionObject


## -description


Plug-ins can use the <b>CreateSessionObject</b> method to create an <a href="https://msdn.microsoft.com/d6f4c66a-79c3-4bc1-889d-ec5715e359ce">ITsSbSession</a> session object.


## -parameters




### -param TargetName [in]

A <b>BSTR</b> variable that contains the target name.


### -param UserName [in]

A <b>BSTR</b> variable that contains the user name.


### -param Domain [in]

A <b>BSTR</b> variable that contains the domain.


### -param SessionId [in]

A <b>DWORD</b> variable that contains the session ID.


### -param ppSession [out]

A pointer to a pointer to the new session object. When you have finished using the object, release it by calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a>



<a href="https://msdn.microsoft.com/d6f4c66a-79c3-4bc1-889d-ec5715e359ce">ITsSbSession</a>
 

 

