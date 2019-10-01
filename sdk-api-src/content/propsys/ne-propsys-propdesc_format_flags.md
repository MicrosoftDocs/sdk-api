---
UID: NE:propsys.PROPDESC_FORMAT_FLAGS
title: PROPDESC_FORMAT_FLAGS (propsys.h)
author: windows-sdk-content
description: Used by property description helper functions, such as PSFormatForDisplay, to indicate the format of a property string.
old-location: properties\PROPDESC_FORMAT_FLAGS.htm
tech.root: properties
ms.assetid: 4425d97f-2530-40d4-ba1a-06bc85f2f567
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PDFF_ALWAYSKB, PDFF_DEFAULT, PDFF_FILENAME, PDFF_HIDEDATE, PDFF_HIDETIME, PDFF_LONGDATE, PDFF_LONGTIME, PDFF_NOAUTOREADINGORDER, PDFF_PREFIXNAME, PDFF_READONLY, PDFF_RELATIVEDATE, PDFF_RESERVED_RIGHTTOLEFT, PDFF_SHORTDATE, PDFF_SHORTTIME, PDFF_USEEDITINVITATION, PROPDESC_FORMAT_FLAGS, PROPDESC_FORMAT_FLAGS enumeration [Windows Properties], _shell_PROPDESC_FORMAT_FLAGS, properties.PROPDESC_FORMAT_FLAGS, propsys/PDFF_ALWAYSKB, propsys/PDFF_DEFAULT, propsys/PDFF_FILENAME, propsys/PDFF_HIDEDATE, propsys/PDFF_HIDETIME, propsys/PDFF_LONGDATE, propsys/PDFF_LONGTIME, propsys/PDFF_NOAUTOREADINGORDER, propsys/PDFF_PREFIXNAME, propsys/PDFF_READONLY, propsys/PDFF_RELATIVEDATE, propsys/PDFF_RESERVED_RIGHTTOLEFT, propsys/PDFF_SHORTDATE, propsys/PDFF_SHORTTIME, propsys/PDFF_USEEDITINVITATION, propsys/PROPDESC_FORMAT_FLAGS, shell.PROPDESC_FORMAT_FLAGS
ms.topic: enum
f1_keywords: 
 - "propsys/PROPDESC_FORMAT_FLAGS"
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propsys.h
api_name:
 - PROPDESC_FORMAT_FLAGS
targetos: Windows
req.typenames: PROPDESC_FORMAT_FLAGS
req.redist: 
ms.custom: 19H1
---

# PROPDESC_FORMAT_FLAGS enumeration


## -description


Used by property description helper functions, such as <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-psformatfordisplay">PSFormatForDisplay</a>, to indicate the format of a property string.


## -enum-fields




### -field PDFF_DEFAULT

Use the format settings specified in the property's .propdesc file.


### -field PDFF_PREFIXNAME

Precede the value with the property's display name. If the <i>hideLabelPrefix</i> attribute of the <a href="https://docs.microsoft.com/windows/desktop/properties/propdesc-schema-labelinfo">labelInfo</a> element in the property's .propinfo file is set to <b>true</b>, then this flag is ignored.


### -field PDFF_FILENAME

Treat the string as a file name.


### -field PDFF_ALWAYSKB

Byte sizes are always displayed in KB, regardless of size. This enables clean alignment of the values in the column. This flag applies only to properties that have been declared as type <b>Integer</b> in the <i>displayType</i> attribute of the <a href="https://docs.microsoft.com/windows/desktop/properties/propdesc-schema-displayinfo">displayInfo</a> element in the property's .propinfo file. This flag overrides the <a href="https://docs.microsoft.com/windows/desktop/properties/propdesc-schema-numberformat">numberFormat</a> setting.


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



