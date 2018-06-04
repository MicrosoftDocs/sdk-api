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

# CM_STATE enumeration


## -description


Specifies column state values. Used by members of the <a href="https://msdn.microsoft.com/d01cacd8-1867-4f44-bbc3-876bd727c0fe">IColumnManager</a> interface through the <a href="https://msdn.microsoft.com/b4437aa7-9682-4819-a353-936179e84005">CM_COLUMNINFO</a> structure.


## -enum-fields




### -field CM_STATE_NONE

The column is not currently displayed.


### -field CM_STATE_VISIBLE

The column is currently displayed.


### -field CM_STATE_FIXEDWIDTH

The column cannot be resized.


### -field CM_STATE_NOSORTBYFOLDERNESS

Do not sort folders separately.


### -field CM_STATE_ALWAYSVISIBLE

The column cannot be hidden.

