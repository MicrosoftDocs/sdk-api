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

# TreeScope enumeration


## -description


Contains values that specify the scope of various operations in the Microsoft UI Automation tree.


## -enum-fields




### -field TreeScope_None

The scope excludes the subtree from the search.


### -field TreeScope_Element

The scope includes the element itself.


### -field TreeScope_Children

The scope includes children of the element.


### -field TreeScope_Descendants

The scope includes children and more distant descendants of the element.


### -field TreeScope_Parent

The scope includes the parent of the element.


### -field TreeScope_Ancestors

The scope includes the parent and more distant ancestors of the element.


### -field TreeScope_Subtree

The scope includes the element and all its descendants. This flag is a combination of the TreeScope_Element and TreeScope_Descendants values.


## -see-also




<a href="https://msdn.microsoft.com/15ceca71-33e8-4d66-afd6-3d50fe81c127">AddAutomationEventHandler</a>



<a href="https://msdn.microsoft.com/2623a48e-8818-486c-9bde-b218cde49189">AddPropertyChangedEventHandler</a>



<a href="https://msdn.microsoft.com/0d3cf5c3-5d0e-4214-a9fc-8b0132ad9b77">AddPropertyChangedEventHandlerNativeArray</a>



<a href="https://msdn.microsoft.com/671049a4-50cf-49df-9028-7af38629b7a9">AddStructureChangedEventHandler</a>



<a href="https://msdn.microsoft.com/ead73c6d-7fb8-4e00-b027-5d747268af08">FindAll</a>



<a href="https://msdn.microsoft.com/acf16f88-2b68-4fd4-b715-b3a61340bdd0">FindAllBuildCache</a>



<a href="https://msdn.microsoft.com/84098431-46e8-49bd-a258-337ad1d68f91">FindFirst</a>



<a href="https://msdn.microsoft.com/ecb10fbf-ff1d-4bd0-b036-1050560d82fe">FindFirstBuildCache</a>



<b>Reference</b>
 

 

