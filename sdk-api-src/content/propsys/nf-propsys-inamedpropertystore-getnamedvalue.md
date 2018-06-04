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

# INamedPropertyStore::GetNamedValue


## -description


Gets the value of a named property from the named property store.


## -parameters




### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to the property name, as a Unicode string, of the property in the named property store.


### -param ppropvar






#### - pv [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this method returns, contains a pointer to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that holds the property's value.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.
                
                    

If the property named in <i>pszName</i> is not found in the property store, this method returns S_OK and the <i>pv</i> member is set to VT_EMPTY.



