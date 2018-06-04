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

# IObjectProvider::QueryObject


## -description


Queries for a specified object.


## -parameters




### -param guidObject [in]

Type: <b>REFGUID</b>

A reference to the <b>GUID</b> used to identify the object.


### -param riid [in]

Type: <b>REFIID</b>

Specifies the desired interface ID.


### -param ppvOut [out]

Type: <b>void**</b>

On success, contains the address of a pointer to the object specified by <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Object implementers that want to enable the discovery of other objects that they can produce or that they hold should implement <b>IObjectProvider::QueryObject</b> and publish the <b>GUID</b> values that name those objects for clients of that object. Note that objects should not pass on the request for an object to other objects like <a href="_inet_IServiceProvider_QueryService_Method">QueryService</a>.



