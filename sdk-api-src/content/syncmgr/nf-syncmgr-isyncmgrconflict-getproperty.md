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

# ISyncMgrConflict::GetProperty


## -description


Gets a conflict property, given a property key.


## -parameters




### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

A reference to the property key for which the property is being requested. Any property key is valid here, including but not limited to the following values.



#### PKEY_ItemNameDisplay

Name of the conflict.



#### PKEY_Sync_ConflictDescription

Summary of the conflict.



#### PKEY_Sync_HandlerID

Sync handler that created the conflict.



#### PKEY_Sync_ItemID

Sync item that created the conflict.



#### PKEY_DateModified

Time the conflict was detected.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this method returns, contains a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains the requested property.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The properties returned are properties of the conflict and not of the <b>IShellItems</b> that are in conflict.

If the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> referenced in <i>propkey</i> is not present in the property store, this method returns S_OK and the <b>vt</b> member of the structure pointed to by <i>ppropvar</i> is set to VT_EMPTY.



