---
UID: NE:fsrmenums._FsrmPropertyDefinitionType
title: FsrmPropertyDefinitionType (fsrmenums.h)
description: Defines the types of file classification properties that you can define.
helpviewer_keywords: ["FsrmPropertyDefinitionType","FsrmPropertyDefinitionType enumeration [File Server Resource Manager]","FsrmPropertyDefinitionType_Bool","FsrmPropertyDefinitionType_Date","FsrmPropertyDefinitionType_Int","FsrmPropertyDefinitionType_MultiChoiceList","FsrmPropertyDefinitionType_MultiString","FsrmPropertyDefinitionType_OrderedList","FsrmPropertyDefinitionType_SingleChoiceList","FsrmPropertyDefinitionType_String","FsrmPropertyDefinitionType_Unknown","fs.fsrmpropertydefinitiontype","fsrm.fsrmpropertydefinitiontype","fsrmenums/FsrmPropertyDefinitionType","fsrmenums/FsrmPropertyDefinitionType_Bool","fsrmenums/FsrmPropertyDefinitionType_Date","fsrmenums/FsrmPropertyDefinitionType_Int","fsrmenums/FsrmPropertyDefinitionType_MultiChoiceList","fsrmenums/FsrmPropertyDefinitionType_MultiString","fsrmenums/FsrmPropertyDefinitionType_OrderedList","fsrmenums/FsrmPropertyDefinitionType_SingleChoiceList","fsrmenums/FsrmPropertyDefinitionType_String","fsrmenums/FsrmPropertyDefinitionType_Unknown"]
old-location: fsrm\fsrmpropertydefinitiontype.htm
tech.root: fsrm
ms.assetid: 618335a2-2b37-43e2-adaa-2a6d06464627
ms.date: 12/05/2018
ms.keywords: FsrmPropertyDefinitionType, FsrmPropertyDefinitionType enumeration [File Server Resource Manager], FsrmPropertyDefinitionType_Bool, FsrmPropertyDefinitionType_Date, FsrmPropertyDefinitionType_Int, FsrmPropertyDefinitionType_MultiChoiceList, FsrmPropertyDefinitionType_MultiString, FsrmPropertyDefinitionType_OrderedList, FsrmPropertyDefinitionType_SingleChoiceList, FsrmPropertyDefinitionType_String, FsrmPropertyDefinitionType_Unknown, fs.fsrmpropertydefinitiontype, fsrm.fsrmpropertydefinitiontype, fsrmenums/FsrmPropertyDefinitionType, fsrmenums/FsrmPropertyDefinitionType_Bool, fsrmenums/FsrmPropertyDefinitionType_Date, fsrmenums/FsrmPropertyDefinitionType_Int, fsrmenums/FsrmPropertyDefinitionType_MultiChoiceList, fsrmenums/FsrmPropertyDefinitionType_MultiString, fsrmenums/FsrmPropertyDefinitionType_OrderedList, fsrmenums/FsrmPropertyDefinitionType_SingleChoiceList, fsrmenums/FsrmPropertyDefinitionType_String, fsrmenums/FsrmPropertyDefinitionType_Unknown
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: FsrmPropertyDefinitionType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmPropertyDefinitionType
 - fsrmenums/_FsrmPropertyDefinitionType
 - FsrmPropertyDefinitionType
 - fsrmenums/FsrmPropertyDefinitionType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmPropertyDefinitionType
---

# FsrmPropertyDefinitionType enumeration


## -description

Defines the types of file classification properties that you can define.

## -enum-fields

### -field FsrmPropertyDefinitionType_Unknown:0

The type is unknown. Do not use this value.

### -field FsrmPropertyDefinitionType_OrderedList:1

A classification property that defines an ordered list of possible string values, one of which may be 
       assigned to the property.

The aggregation policy for this type is to use the order in which the items are added to the list to 
       determine which value to use if the property exists and contains a value that is different from the rule's 
       value. For example, if the list contains "HBI", "MBI", and 
       "LBI", and one source specifies "MBI" and the other source specifies 
       "HBI", the property value is set to "HBI" because it appears before 
       "MBI" in the list.

You can use the following comparison operators with this type (see 
       <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmpropertyconditiontype">FsrmPropertyConditionType</a>): Equal, Not equal, 
       Greater than, Less than, Exists, and Not exists.

### -field FsrmPropertyDefinitionType_MultiChoiceList:2

A classification property that defines a list of possible string values, one or more of which may be assigned 
       to the property. Use the vertical bar character (|) to delimit the strings.

The aggregation policy for this type is to concatenate the values from each source, consolidating any 
       duplicates. For example, if the list of possible values contains "Cat1", 
       "Cat2", "Cat3", and "Cat4", and one source specifies 
       "Cat3" and another source specifies "Cat1", the property value is set to 
       "Cat1|Cat3".

You can use the following comparison operators with this type (see 
       <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmpropertyconditiontype">FsrmPropertyConditionType</a>): Equal, Not equal, 
       Contains, Contained in, Exists, and Not exists.

### -field FsrmPropertyDefinitionType_SingleChoiceList:3

A classification property that defines a list of possible string values, only one of which may be assigned 
       to the property.

No aggregation is available for this type.

You can use the following comparison operators with this type (see 
       <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmpropertyconditiontype">FsrmPropertyConditionType</a>): Equal, Not equal, 
       Exists, and Not exists.

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This file classification property type is not supported before Windows Server 2012.

### -field FsrmPropertyDefinitionType_String:4

A classification property that contains an arbitrary string value.

The aggregation policy is to fail if two sources do not specify the same value.

You can use the following comparison operators with this type (see 
       <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmpropertyconditiontype">FsrmPropertyConditionType</a>): Equal, Not equal, 
       Greater than, Less than, Contains, Contained in, Start with, End with, Prefix of, Suffix of, Exists, and Not 
       exists.

### -field FsrmPropertyDefinitionType_MultiString:5

A classification property that contains one or more arbitrary string values. Use the vertical bar character 
       (|) to delimit the strings.

The aggregation policy is to concatenate the values from each source, consolidating any duplicates. For 
       example if one source specifies "String1|String2" and another source specifies 
       "String1|String3", the property value is set to "String1|String2|String3".

You can use the following comparison operators with this type (see 
       <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmpropertyconditiontype">FsrmPropertyConditionType</a>): Equal, Not equal, 
       Contains, Contained in, Exists, and Not exists.

### -field FsrmPropertyDefinitionType_Int:6

A classification property that contains a decimal integer value expressed as a string.

The aggregation policy is to fail if two sources do not specify the same value.

You can use the following comparison operators with this type (see 
       <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmpropertyconditiontype">FsrmPropertyConditionType</a>): Equal, Not equal, 
       Greater than, Less than, Exists, and Not exists.

### -field FsrmPropertyDefinitionType_Bool:7

A classification property that contains a Boolean value expressed as a string. Use a string value of 
       "0" for <b>False</b> or a string value of "1" for 
       <b>True</b>.

The aggregation policy is to perform a logical <b>OR</b> on the values from each 
       source. For example, if one source specifies <b>True</b> and another source specifies 
       <b>False</b>, the property value is set to <b>True</b>. If two sources 
       both specify <b>False</b>, the property value is set to <b>False</b>.

You can use the following comparison operators with this type (see 
       <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmpropertyconditiontype">FsrmPropertyConditionType</a>): Equal, Not equal, 
       Exists, and Not exists.

### -field FsrmPropertyDefinitionType_Date:8

A classification property that contains a date value. The date value is a 64-bit decimal number (see 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>) expressed as a string.

The aggregation policy is to fail if two sources do not specify the same value.

You can use the following comparison operators with this type (see 
       <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmpropertyconditiontype">FsrmPropertyConditionType</a>): Equal, Not equal, 
       Greater than, Less than, Exists, and Not exists.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertydefinition-get_type">IFsrmPropertyDefinition.Type</a>
