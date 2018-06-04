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

# SHCOLUMNINIT structure


## -description


Passes initialization information to <a href="https://msdn.microsoft.com/4975042d-549e-4032-9f42-468dc7e3c20e">IColumnProvider::Initialize</a>.


## -struct-fields




### -field dwFlags

Type: <b>ULONG</b>

Initialization flags. Reserved. Set to <b>NULL</b>


### -field dwReserved

Type: <b>ULONG</b>

Reserved. Set to <b>NULL</b>.


### -field wszFolder

Type: <b>WCHAR[MAX_PATH]</b>

A pointer to a null-terminated Unicode string with a fully qualified folder path. The string will be empty if multiple folders are specified.

