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

# _WINDOWDATA structure


## -description


Stores window data.


## -struct-fields




### -field dwWindowID

Type: <b>DWORD</b>

The window ID.


### -field uiCP

Type: <b>UINT</b>

The codepage of the current entry.


### -field pidl

Type: <b>PIDLIST_ABSOLUTE</b>

The current PIDL.


### -field lpszUrl

Type: <b>LPWSTR</b>

A pointer to a buffer to hold the window URL.


### -field lpszUrlLocation

Type: <b>LPWSTR</b>

A pointer to a buffer to hold the window URL Location (local anchor).


### -field lpszTitle

Type: <b>LPWSTR</b>

A pointer to a buffer to hold the window title.

