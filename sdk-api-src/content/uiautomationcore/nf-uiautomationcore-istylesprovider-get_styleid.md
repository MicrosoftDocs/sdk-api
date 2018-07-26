---
UID: NF:uiautomationcore.IStylesProvider.get_StyleId
title: IStylesProvider::get_StyleId
author: windows-sdk-content
description: Identifies the visual style of an element in a document.
old-location: winauto\uiauto_istylesprovider_styleid.htm
old-project: WinAuto
ms.assetid: EFFEC853-595C-4304-8EDF-BA80EA8FEC5B
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IStylesProvider interface [Windows Accessibility],StyleId property, IStylesProvider.StyleId, IStylesProvider.get_StyleId, IStylesProvider::StyleId, IStylesProvider::get_StyleId, StyleId property [Windows Accessibility], StyleId property [Windows Accessibility],IStylesProvider interface, get_StyleId, uiautomationcore/IStylesProvider::StyleId, uiautomationcore/IStylesProvider::get_StyleId, winauto.uiauto_istylesprovider_styleid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IStylesProvider.StyleId
 - IStylesProvider.get_StyleId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IStylesProvider::get_StyleId


## -description


Identifies the visual style of an element in a document.

This property is read-only.


## -parameters


## -remarks



A provider should use this property to expose style identifiers that are useful to client applications. For example, a provider might expose the <a href="https://msdn.microsoft.com/library/Hh437309(v=VS.85).aspx">StyleId_Title</a> identifier for an element that represents the title of a presentation. A screen reader could then retrieve the <b>StyleId</b> property, discover that the element is a presentation title, and read the title to the user.

<h3><a id="List_Styles"></a><a id="list_styles"></a><a id="LIST_STYLES"></a>List Styles</h3>
IDs for list styles are supported starting with Windows 8.1. 

These styles should be applied at a paragraph level; all text that is part of a list item should have one of these styles applied to it.

When bullet styles are mixed within a list, the <b>BulletedList</b> style should be applied to the whole range, and the <a href="https://msdn.microsoft.com/fb4e4df3-ef0d-43e9-abeb-01e328c32692">BulletStyle</a> attribute value (property identified by <b>UIA_BulletStyleAttributeId</b>) should be mixed according to breakdown of different bullet types within the range.

When nested lists contain bullets also (perhaps of a different type than the main list), the <b>BulletedList</b> style would again be applied to the whole range, and the <b>BulletStyle</b> attribute value is whatever the nested bullet style is (for the range covering the nested list).




## -see-also




<a href="https://msdn.microsoft.com/fb4e4df3-ef0d-43e9-abeb-01e328c32692">BulletStyle</a>



<a href="https://msdn.microsoft.com/9424a6cd-9f4b-4653-9737-4afb9cfb510f">IStylesProvider</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

