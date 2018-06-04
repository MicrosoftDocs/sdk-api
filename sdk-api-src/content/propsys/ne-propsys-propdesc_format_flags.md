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

# PROPDESC_FORMAT_FLAGS enumeration


## -description


Used by property description helper functions, such as <a href="shell.PSFormatForDisplay">PSFormatForDisplay</a>, to indicate the format of a property string.


## -enum-fields




### -field PDFF_DEFAULT

Use the format settings specified in the property's .propdesc file.


### -field PDFF_PREFIXNAME

Precede the value with the property's display name. If the <i>hideLabelPrefix</i> attribute of the <a href="shell.propdesc_schema_labelInfo">labelInfo</a> element in the property's .propinfo file is set to <b>true</b>, then this flag is ignored.


### -field PDFF_FILENAME

Treat the string as a file name.


### -field PDFF_ALWAYSKB

Byte sizes are always displayed in KB, regardless of size. This enables clean alignment of the values in the column. This flag applies only to properties that have been declared as type <b>Integer</b> in the <i>displayType</i> attribute of the <a href="shell.propdesc_schema_displayInfo">displayInfo</a> element in the property's .propinfo file. This flag overrides the <a href="shell.propdesc_schema_numberFormat">numberFormat</a> setting.


### -field PDFF_RESERVED_RIGHTTOLEFT

Reserved.


### -field PDFF_SHORTTIME

Display time as "hh:mm am/pm".


### -field PDFF_LONGTIME

Display time as "hh:mm:ss am/pm".


### -field PDFF_HIDETIME

Hide the time portion of <code>datetime</code>.


### -field PDFF_SHORTDATE

Display date as "MM/DD/YY". For example, "03/21/04".


### -field PDFF_LONGDATE

Display date as "DayOfWeek, Month day, year". For example, "Monday, March 21, 2009".


### -field PDFF_HIDEDATE

Hide the date portion of <code>datetime</code>.


### -field PDFF_RELATIVEDATE

Use friendly date descriptions. For example, "Yesterday".


### -field PDFF_USEEDITINVITATION

Return the invitation text if formatting failed or the value was empty. Invitation text is text displayed in a text box as a cue for the user, such as "Enter your name". Formatting can fail if the data entered is not of an expected type, such as when alpha characters have been entered in a phone-number field.


### -field PDFF_READONLY

If this flag is used, the <b>PDFF_USEEDITINVITATION</b> flag must also be specified. When the formatting flags are <b>PDFF_READONLY</b> | <b>PDFF_USEEDITINVITATION</b> and the algorithm would have shown invitation text, a string is returned that indicates the value is "Unknown" instead of returning the invitation text.


### -field PDFF_NOAUTOREADINGORDER

Do not detect reading order automatically. Useful when converting to ANSI to omit the Unicode reading order characters. However, reading order characters for some values are still returned.


## -remarks



These values are defined in propsys.h and propsys.idl.

Typically use one, or a bitwise combination of these flags to specify format. Some flags are mutually exclusive, for example PDFF_SHORTTIME  | PDFF_LONGTIME | PDFF_HIDETIME, is not allowed. 



