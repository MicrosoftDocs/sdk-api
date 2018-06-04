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

# __MIDL___MIDL_itf_vmr9_0000_0008_0001 enumeration


## -description



The <code>VMR9RenderPrefs</code> enumeration type specifies basic rendering preferences for the VMR-9. It is used with the <a href="https://msdn.microsoft.com/b82a9dbe-aa86-4153-945b-fe8968faa5ca">IVMRFilterConfig9::GetRenderingPrefs</a> and <a href="https://msdn.microsoft.com/ce274528-c759-4b43-80c7-0ba1e1275b7d">IVMRFilterConfig9::SetRenderingPrefs</a> methods.




## -enum-fields




### -field RenderPrefs9_DoNotRenderBorder

Indicates that the application paints the color keyed areas.


### -field RenderPrefs9_Mask

Bitwise <b>OR</b> of all flags; not used by applications.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

