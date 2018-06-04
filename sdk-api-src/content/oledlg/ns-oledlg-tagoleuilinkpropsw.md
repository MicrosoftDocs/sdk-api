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

# tagOLEUILINKPROPSW structure


## -description


Contains information that is used to initialize the <b>Link</b> tab of the <b>Object Properties</b> dialog box. A reference to it is passed in as part of the <a href="https://msdn.microsoft.com/7a6216d6-061f-48c3-8e3f-5f3e5a63ffb3">OLEUIOBJECTPROPS</a> structure to the <a href="https://msdn.microsoft.com/591f6056-2e5f-4e58-8806-9a0093de2463">OleUIObjectProperties</a> function. This tab shows the location, update status, and update time for a link. It allows the user to change the source of the link, toggle its update status between automatic and manual update, open the source, force an update of the link, or break the link (convert it to a static picture).


## -struct-fields




### -field cbStruct

The size of the structure, in bytes.


### -field dwFlags

Contains in/out flags specific to the <b>Links</b> page.


### -field dwReserved1

This member is reserved.


### -field lpfnHook

Pointer to the hook callback (not used in this dialog box).


### -field lCustData

Custom data to pass to hook (not used in this dialog box).


### -field dwReserved2

This member is reserved.


### -field lpOP

Used internally.


## -see-also




<a href="https://msdn.microsoft.com/7a6216d6-061f-48c3-8e3f-5f3e5a63ffb3">OLEUIOBJECTPROPS</a>



<a href="https://msdn.microsoft.com/591f6056-2e5f-4e58-8806-9a0093de2463">OleUIObjectProperties</a>
 

 

