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

# EXTRASEARCH structure


## -description


Used by an <a href="https://msdn.microsoft.com/63b71cd2-483b-482f-b3f4-6d5c937e7708">IEnumExtraSearch</a> enumerator object to return information on the search objects supported by a Shell Folder object.


## -struct-fields




### -field guidSearch

Type: <b>GUID</b>

A search object's GUID.


### -field wszFriendlyName

Type: <b>WCHAR[80]</b>

A Unicode string containing the search object's friendly name. It will be used to identify the search engine on the Search Assistant menu.


### -field wszUrl

Type: <b>WCHAR[2084]</b>

The URL that will be displayed in the search pane.

