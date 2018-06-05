---
UID: NS:uiautomationcore.UiaChangeInfo
title: UiaChangeInfo
author: windows-sdk-content
description: Contains data about a UI Automation change that occurred.
old-location: winauto\uiachangeinfo.htm
old-project: WinAuto
ms.assetid: 28C0C0DE-7ED2-4D01-B532-E56AD81AE8D0
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: PUiaChangeInfo, PUiaChangeInfo structure pointer [Windows Accessibility], UiaChangeInfo, UiaChangeInfo structure [Windows Accessibility], uiautomationcore/PUiaChangeInfo, uiautomationcore/UiaChangeInfo, winauto.uiachangeinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: uiautomationcore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	UIAutomationCore.h
api_name:
-	UiaChangeInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# UiaChangeInfo structure


## -description


Contains data about a UI Automation change that occurred.


## -struct-fields




### -field uiaId

Identifies the type of change info. Possible values are all the values of <b>Change Indentifiers</b>, <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>, <a href="https://msdn.microsoft.com/67d86817-6a3f-4047-88d9-34f33f52a563">Text Attribute Identifiers</a>, <a href="https://msdn.microsoft.com/46948B7C-EC9F-4B55-B769-62EE8BE11D33">Annotation Type Identifiers</a> and <a href="https://msdn.microsoft.com/BC06F8B6-3A2B-46BF-A8A6-6BA69A72738A">Style Identifiers</a>.


### -field payload

Information about the type of change that occurred.


### -field extraInfo

Detailed information about the change that occurred.


## -remarks



The provider can call <a href="https://msdn.microsoft.com/AA6F1F6E-3EE9-44A6-B1AE-B08013DC1E37">UiaRaiseChangesEvent</a> and pass in an array of <b>UiaChangeInfo</b> structs to notify clients of a related group of changes.  The <b>payload</b> and <b>extraInfo</b> will vary depending on the <b>uiaId</b> populated in the <b>UiaChangeInfo</b> struct.

If there are multiple of any of these event types multiple <b>UiaChangeInfo</b> structs would be created.  Below is a description of what these are for each pair of values.

<table>
<tr>
<th>UiaId</th>
<th>payload</th>
<th>extraInfo</th>
</tr>
<tr>
<td>
<b>UIA_SummaryChangeId</b>

</td>
<td>
VT_BSTR

A string describing the meaning of the change from an application point of view.

</td>
<td>
A constant ID value from the provider indicating the meaning of this event.

</td>
</tr>
<tr>
<td>
For UIA property changes, identified in the <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a> section.

</td>
<td>
Type is the type of the property and the value is the new value of the property.

</td>
<td>
 

</td>
</tr>
<tr>
<td>
For text attributes changes, identified in the <a href="https://msdn.microsoft.com/67d86817-6a3f-4047-88d9-34f33f52a563">Text Attribute Identifiers</a> section, <b>extraInfo</b> is not used.

</td>
<td>
Type is the type of the attribute and the value is the new value of the attribute.

</td>
<td>
 

</td>
</tr>
<tr>
<td>
For annotation changes, identified in the <a href="https://msdn.microsoft.com/46948B7C-EC9F-4B55-B769-62EE8BE11D33">Annotation Type Identifiers</a> section, <b>extraInfo</b> is not used.

</td>
<td>
VT_BSTR

For text, the characters from the range to which the annotation  applies.

</td>
<td>
 

</td>
</tr>
<tr>
<td>
For style changes, identified in the <a href="https://msdn.microsoft.com/BC06F8B6-3A2B-46BF-A8A6-6BA69A72738A">Style Identifiers</a> section, <b>extraInfo</b> is not used.

</td>
<td>
VT_BSTR

For text, the characters from the range to which the style applies.

</td>
<td>
 

</td>
</tr>
</table>
 



