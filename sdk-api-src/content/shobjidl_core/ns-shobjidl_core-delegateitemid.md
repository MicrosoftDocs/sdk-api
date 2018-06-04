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

# DELEGATEITEMID structure


## -description


Used by delegate folders in place of a standard <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -struct-fields




### -field cbSize

Type: <b>WORD</b>

The size, in bytes, of this structure.


### -field wOuter

Type: <b>WORD</b>

Private data owned by the delegating (outer) folder.


### -field cbInner

Type: <b>WORD</b>

The size, in bytes, of the delegate's data. The first <b>cbInner</b> bytes of the <b>rgb</b> array contain this data. The remaining data in <b>rgb</b> belongs to the outer folder.


### -field rgb

Type: <b>BYTE[1]</b>

An array holding the inner folder's data, which is opaque to the outer folder, followed by outer folder's data.

