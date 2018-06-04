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

# IMAGEHLP_EXTENDED_OPTIONS enumeration


## -description


Lists the extended symbol options that you can get and set by using the <a href="https://msdn.microsoft.com/3D6D5E31-ECCB-48B2-A46B-0BB2D7A2DEC0">SymGetExtendedOption</a> and <a href="https://msdn.microsoft.com/25756250-D2B4-4D5A-BED0-238C34C18093">SymSetExtendedOption</a> functions.


## -enum-fields




### -field SYMOPT_EX_DISABLEACCESSTIMEUPDATE

Turns off explicit updates to the last access time of a symbol that is loaded. By default, DbgHelp updates the last access time of a symbol file that is consumed so that a symbol cache can be maintained by using a least recently used mechanism.


### -field SYMOPT_EX_MAX

Unused.


## -see-also




<a href="https://msdn.microsoft.com/3D6D5E31-ECCB-48B2-A46B-0BB2D7A2DEC0">SymGetExtendedOption</a>



<a href="https://msdn.microsoft.com/25756250-D2B4-4D5A-BED0-238C34C18093">SymSetExtendedOption</a>
 

 

