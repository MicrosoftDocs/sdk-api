---
UID: NS:uiautomationcore.UiaChangeInfo
title: UiaChangeInfo (uiautomationcore.h)
description: Contains data about a UI Automation change that occurred.
helpviewer_keywords: ["PUiaChangeInfo","PUiaChangeInfo structure pointer [Windows Accessibility]","UiaChangeInfo","UiaChangeInfo structure [Windows Accessibility]","uiautomationcore/PUiaChangeInfo","uiautomationcore/UiaChangeInfo","winauto.uiachangeinfo"]
old-location: winauto\uiachangeinfo.htm
tech.root: WinAuto
ms.assetid: 28C0C0DE-7ED2-4D01-B532-E56AD81AE8D0
ms.date: 12/05/2018
ms.keywords: PUiaChangeInfo, PUiaChangeInfo structure pointer [Windows Accessibility], UiaChangeInfo, UiaChangeInfo structure [Windows Accessibility], uiautomationcore/PUiaChangeInfo, uiautomationcore/UiaChangeInfo, winauto.uiachangeinfo
req.header: uiautomationcore.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaChangeInfo
 - uiautomationcore/UiaChangeInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCore.h
api_name:
 - UiaChangeInfo
---

# UiaChangeInfo structure


## -description

Contains data about a UI Automation change that occurred.

## -struct-fields

### -field uiaId

Identifies the type of change info. Possible values are all the values of <b>Change Identifiers</b>, <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>, <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">Text Attribute Identifiers</a>, <a href="/windows/desktop/WinAuto/uiauto-annotation-type-identifiers">Annotation Type Identifiers</a> and <a href="/windows/desktop/WinAuto/uiauto-style-identifiers">Style Identifiers</a>.

### -field payload

Information about the type of change that occurred.

### -field extraInfo

Detailed information about the change that occurred.

## -remarks

The provider can call <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaraisechangesevent">UiaRaiseChangesEvent</a> and pass in an array of <b>UiaChangeInfo</b> structs to notify clients of a related group of changes.  The <b>payload</b> and <b>extraInfo</b> will vary depending on the <b>uiaId</b> populated in the <b>UiaChangeInfo</b> struct.

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
For UIA property changes, identified in the <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a> section.

</td>
<td>
Type is the type of the property and the value is the new value of the property.

</td>
<td>
 

</td>
</tr>
<tr>
<td>
For text attributes changes, identified in the <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">Text Attribute Identifiers</a> section, <b>extraInfo</b> is not used.

</td>
<td>
Type is the type of the attribute and the value is the new value of the attribute.

</td>
<td>
 

</td>
</tr>
<tr>
<td>
For annotation changes, identified in the <a href="/windows/desktop/WinAuto/uiauto-annotation-type-identifiers">Annotation Type Identifiers</a> section, <b>extraInfo</b> is not used.

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
For style changes, identified in the <a href="/windows/desktop/WinAuto/uiauto-style-identifiers">Style Identifiers</a> section, <b>extraInfo</b> is not used.

</td>
<td>
VT_BSTR

For text, the characters from the range to which the style applies.

</td>
<td>
 

</td>
</tr>
</table>