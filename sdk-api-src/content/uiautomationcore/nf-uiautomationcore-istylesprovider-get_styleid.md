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

# IStylesProvider::get_StyleId


## -description


Identifies the visual style of an element in a document.

This property is read-only.


## -parameters


## -remarks



A provider should use this property to expose style identifiers that are useful to client applications. For example, a provider might expose the <a href="uiauto_style_identifiers.htm">StyleId_Title</a> identifier for an element that represents the title of a presentation. A screen reader could then retrieve the <b>StyleId</b> property, discover that the element is a presentation title, and read the title to the user.

<h3><a id="List_Styles"></a><a id="list_styles"></a><a id="LIST_STYLES"></a>List Styles</h3>
IDs for list styles are supported starting with Windows 8.1. 

These styles should be applied at a paragraph level; all text that is part of a list item should have one of these styles applied to it.

When bullet styles are mixed within a list, the <b>BulletedList</b> style should be applied to the whole range, and the <a href="https://msdn.microsoft.com/fb4e4df3-ef0d-43e9-abeb-01e328c32692">BulletStyle</a> attribute value (property identified by <b>UIA_BulletStyleAttributeId</b>) should be mixed according to breakdown of different bullet types within the range.

When nested lists contain bullets also (perhaps of a different type than the main list), the <b>BulletedList</b> style would again be applied to the whole range, and the <b>BulletStyle</b> attribute value is whatever the nested bullet style is (for the range covering the nested list).




## -see-also




<a href="https://msdn.microsoft.com/fb4e4df3-ef0d-43e9-abeb-01e328c32692">BulletStyle</a>



<a href="https://msdn.microsoft.com/9424a6cd-9f4b-4653-9737-4afb9cfb510f">IStylesProvider</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

