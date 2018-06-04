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

# MENUITEMTEMPLATEHEADER structure


## -description


Defines the header for a menu template. A complete menu template consists of a header and one or more menu item lists. 


## -struct-fields




### -field versionNumber

Type: <b>WORD</b>

The version number. This member must be zero. 


### -field offset

Type: <b>WORD</b>

The offset, in bytes, from the end of the header. The menu item list begins at this offset. Usually, this member is zero, and the menu item list follows immediately after the header. 


## -remarks



One or more <a href="https://msdn.microsoft.com/9329aee3-83be-4409-98f4-e135f39c0f01">MENUITEMTEMPLATE</a> structures are combined to form the menu item list. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/01736486-6dee-43fe-80a7-06c4cf13a23e">LoadMenuIndirect</a>



<a href="https://msdn.microsoft.com/9329aee3-83be-4409-98f4-e135f39c0f01">MENUITEMTEMPLATE</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>
 

 

