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

# tagOFN_NT4W structure


## -description


The <b>OPENFILENAME_NT4</b> structure is identical to <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> with _WIN32_WINNT set to 0x0400. It allows an application to take advantage of other post-Microsoft Windows NT 4.0 features while running on Microsoft Windows NT 4.0. Also, MFC42 applications must use <b>OPENFILENAME_NT4</b> to avoid heap corruption. This is because Microsoft Foundation Classes (MFC) has classes with embedded <b>OPENFILENAME</b> structures, and you must use the same structure size.
<div class="alert"><b>Note</b>  This structure is provided only for compatibility.</div><div> </div>

## -struct-fields

