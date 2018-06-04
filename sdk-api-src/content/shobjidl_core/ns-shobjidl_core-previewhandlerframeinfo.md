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

# PREVIEWHANDLERFRAMEINFO structure


## -description


Accelerator table structure. Used by <a href="https://msdn.microsoft.com/953b7571-0da1-4e31-bb6f-1761f8103c6e">IPreviewHandlerFrame::GetWindowContext</a>.


## -struct-fields




### -field haccel

Type: <b>HACCEL</b>

A handle to the accelerator table.


### -field cAccelEntries

Type: <b>UINT</b>

The number of entries in the accelerator table.

