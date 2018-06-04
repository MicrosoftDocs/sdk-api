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

# IShellIconOverlayIdentifier::GetPriority


## -description


Specifies the priority of an icon overlay.


## -parameters




### -param pPriority [out]

Type: <b>int*</b>

The address of a value that indicates the priority of the overlay identifier. Possible values range from zero to 100, with zero the highest priority.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error code otherwise.




## -remarks



If more than one icon overlay is available for an object, the one with highest priority is chosen. The Shell has a set of internal rules that determine priority for many cases. The value returned by <b>GetPriority</b> is used for those cases in which the Shell's internal rules do not apply. Typically, you should set the value to zero. However, the priority value is useful when you have implemented two or more icon overlay handlers that can request icon overlay icons for the same object. By setting the priority values appropriately, you can specify which of the requested icon overlays will be displayed.
      




## -see-also




<a href="https://msdn.microsoft.com/c093bc13-def7-411d-b741-50996ffad84b">IShellIconOverlayIdentifier</a>
 

 

