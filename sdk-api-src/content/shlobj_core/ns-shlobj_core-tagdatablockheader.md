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

# tagDATABLOCKHEADER structure


## -description


Serves as the header for some of the extra data structures used by <a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the extra data block.


### -field dwSignature

Type: <b>DWORD</b>

A signature that identifies the type of data block that follows the header.


## -see-also




<a href="https://msdn.microsoft.com/016c539e-6035-4752-99b6-71e2d7199bf0">EXP_DARWIN_LINK</a>



<a href="https://msdn.microsoft.com/02542cd4-be8f-45c0-ad0f-e1e39a45f5de">NT_CONSOLE_PROPS</a>



<a href="https://msdn.microsoft.com/2f22676d-2b46-4a94-9517-64d1caeead43">NT_FE_CONSOLE_PROPS</a>
 

 

