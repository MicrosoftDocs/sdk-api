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

# SHGetPropertyStoreFromIDList function


## -description


Retrieves an object that supports <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> or related interfaces from a pointer to an item identifier list (PIDL).


## -parameters




### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to an item ID list.


### -param flags [in]

Type: <b><a href="shell.GETPROPERTYSTOREFLAGS">GETPROPERTYSTOREFLAGS</a></b>

One or more values from the <a href="shell.GETPROPERTYSTOREFLAGS">GETPROPERTYSTOREFLAGS</a> constants. This parameter can also be <b>NULL</b>.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired interface ID.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> or a related interface. 

