---
UID: NF:ocidl.IObjectWithSite.SetSite
title: IObjectWithSite::SetSite
author: windows-driver-content
description: Enables a container to pass an object a pointer to the interface for its site.
old-location: com\iobjectwithsite_setsite.htm
old-project: com
ms.assetid: 5e95b2a6-85b3-4899-9e23-54ed9e69e821
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IObjectWithSite interface [COM],SetSite method, IObjectWithSite.SetSite, IObjectWithSite::SetSite, SetSite, SetSite method [COM], SetSite method [COM],IObjectWithSite interface, _ole_iobjectwithsite_setsite, com.iobjectwithsite_setsite, ocidl/IObjectWithSite::SetSite
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IObjectWithSite.SetSite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IObjectWithSite::SetSite


## -description


Enables a container to pass an object a pointer to the interface for its site.


## -parameters




### -param pUnkSite [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface pointer of the site managing this object. If <b>NULL</b>, the object should call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on any existing site at which point the object no longer knows its site.


## -returns



This method returns S_OK on success.




## -remarks



The object should hold onto this pointer, calling <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a> in doing so. If the object already has a site, it should call that existing site's <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a>, save the new site pointer, and call the new site's <b>IUnknown::AddRef</b>.

E_NOTIMPL is not allowedâ€”without implementation of the <b>SetSite</b> method, the <a href="https://msdn.microsoft.com/e688136e-e06b-46ba-bec9-b8db2f9c468d">IObjectWithSite</a> interface is unnecessary.




## -see-also




<a href="https://msdn.microsoft.com/e688136e-e06b-46ba-bec9-b8db2f9c468d">IObjectWithSite</a>
 

 

