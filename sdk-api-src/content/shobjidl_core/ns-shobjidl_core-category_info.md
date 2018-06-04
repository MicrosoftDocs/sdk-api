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

# CATEGORY_INFO structure


## -description


Contains category information. A component category is a group of logically-related Component Object Model (COM) classes that share a common category identifier (CATID).


## -struct-fields




### -field cif

Type: <b><a href="https://msdn.microsoft.com/6179ed67-905a-454a-a226-fe1e5070e39f">CATEGORYINFO_FLAGS</a></b>

A flag from <a href="https://msdn.microsoft.com/6179ed67-905a-454a-a226-fe1e5070e39f">CATEGORYINFO_FLAGS</a> that specifies the type of information to retrieve.


### -field wszName

Type: <b>WCHAR[260]</b>

A character array that specifies the name of the category.

