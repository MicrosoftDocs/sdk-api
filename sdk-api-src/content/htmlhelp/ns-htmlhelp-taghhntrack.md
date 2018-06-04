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

# tagHHNTRACK structure


## -description


This structure returns the file name of the current topic and a constant that specifies the user action that is about to occur, such as hiding the Navigation pane by clicking the Hide button on the toolbar. 


## -struct-fields




### -field hdr

Standard <b>WM_NOTIFY</b> header. 


### -field pszCurUrl

A multi-byte, zero-terminated string that specifies the current topic (before the action is taken). 


### -field idAction

Specifies the action the user is about to take. This is an <a href="https://msdn.microsoft.com/E09BFFD7-8E44-47ba-BAFD-4582FF9430A7">HHACT_</a> constant. 


### -field phhWinType

A pointer to the current <a href="https://msdn.microsoft.com/61614318-9785-4f1e-A9E7-366C04DE4FFE">HH_WINTYPE</a> structure. 


## -see-also




<a href="https://msdn.microsoft.com/E75CA82E-9759-47d8-AF84-5842EDAB019D">About structures</a>
 

 

