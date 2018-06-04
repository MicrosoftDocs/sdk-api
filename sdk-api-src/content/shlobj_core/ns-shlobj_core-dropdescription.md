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

# DROPDESCRIPTION structure


## -description


Describes the image and accompanying text for a drop object.


## -struct-fields




### -field type

Type: <b><a href="https://msdn.microsoft.com/eeaf8bd4-25ab-4ec3-9da9-9a72ba3813b9">DROPIMAGETYPE</a></b>

A <a href="https://msdn.microsoft.com/eeaf8bd4-25ab-4ec3-9da9-9a72ba3813b9">DROPIMAGETYPE</a> indicating the stock image to use.


### -field szMessage

Type: <b>WCHAR[MAX_PATH]</b>

Text such as "Move to %1".


### -field szInsert

Type: <b>WCHAR[MAX_PATH]</b>

Text such as "Documents", inserted as specified by <b>szMessage</b>.


## -remarks



Some UI coloring is applied to the text in <b>szInsert</b> if used by specifying %1 in <b>szMessage</b>. The characters %% and %1 are the subset of <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> markers that are processed here.



