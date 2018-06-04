---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUnknown_GetSite function


## -description


Calls the specified object's <a href="https://msdn.microsoft.com/f88ef2b1-63c3-4307-a5e1-b9104c8aef29">IObjectWithSite::GetSite</a> method.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the COM object whose <a href="https://msdn.microsoft.com/f88ef2b1-63c3-4307-a5e1-b9104c8aef29">IObjectWithSite::GetSite</a> method is to be called.


### -param riid [in]

Type: <b>REFIID</b>

The IID of the interface pointer that should be returned in <i>ppvSite</i>.


### -param ppv

TBD




#### - ppvSite [out]

Type: <b>VOID**</b>

The address of the pointer to receive the requested interface pointer. If the function call is successful, <i>ppvSite</i> will contain the requested interface pointer. If no site is available or the requested interface is not supported, <i>ppvSite</i> is set to <b>NULL</b> and the function returns a COM error code.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the site was successfully retrieved or a COM error code otherwise.




## -remarks



This function calls the specified object's <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method to obtain the <a href="https://msdn.microsoft.com/e688136e-e06b-46ba-bec9-b8db2f9c468d">IObjectWithSite</a> interface.  If successful, the function calls the interface's <a href="https://msdn.microsoft.com/f88ef2b1-63c3-4307-a5e1-b9104c8aef29">IObjectWithSite::GetSite</a> method to obtain the site.



