---
UID: NE:fsrmenums._FsrmPropertyConditionType
title: FsrmPropertyConditionType (fsrmenums.h)
description: Defines the possible comparison operations that can be used to determine whether a property value of a file meets a particular condition.
helpviewer_keywords: ["FsrmPropertyConditionType","FsrmPropertyConditionType enumeration [File Server Resource Manager]","FsrmPropertyConditionType_Contain","FsrmPropertyConditionType_ContainedIn","FsrmPropertyConditionType_EndWith","FsrmPropertyConditionType_Equal","FsrmPropertyConditionType_Exist","FsrmPropertyConditionType_GreaterThan","FsrmPropertyConditionType_LessThan","FsrmPropertyConditionType_MatchesPattern","FsrmPropertyConditionType_NotEqual","FsrmPropertyConditionType_NotExist","FsrmPropertyConditionType_PrefixOf","FsrmPropertyConditionType_StartWith","FsrmPropertyConditionType_SuffixOf","FsrmPropertyConditionType_Unknown","fs.fsrmpropertyconditiontype","fsrm.fsrmpropertyconditiontype","fsrm/FsrmPropertyConditionType","fsrm/FsrmPropertyConditionType_Contain","fsrm/FsrmPropertyConditionType_ContainedIn","fsrm/FsrmPropertyConditionType_EndWith","fsrm/FsrmPropertyConditionType_Equal","fsrm/FsrmPropertyConditionType_Exist","fsrm/FsrmPropertyConditionType_GreaterThan","fsrm/FsrmPropertyConditionType_LessThan","fsrm/FsrmPropertyConditionType_MatchesPattern","fsrm/FsrmPropertyConditionType_NotEqual","fsrm/FsrmPropertyConditionType_NotExist","fsrm/FsrmPropertyConditionType_PrefixOf","fsrm/FsrmPropertyConditionType_StartWith","fsrm/FsrmPropertyConditionType_SuffixOf","fsrm/FsrmPropertyConditionType_Unknown"]
old-location: fsrm\fsrmpropertyconditiontype.htm
tech.root: fsrm
ms.assetid: b3b5caab-4d70-4f85-bf53-0344192d3674
ms.date: 12/05/2018
ms.keywords: FsrmPropertyConditionType, FsrmPropertyConditionType enumeration [File Server Resource Manager], FsrmPropertyConditionType_Contain, FsrmPropertyConditionType_ContainedIn, FsrmPropertyConditionType_EndWith, FsrmPropertyConditionType_Equal, FsrmPropertyConditionType_Exist, FsrmPropertyConditionType_GreaterThan, FsrmPropertyConditionType_LessThan, FsrmPropertyConditionType_MatchesPattern, FsrmPropertyConditionType_NotEqual, FsrmPropertyConditionType_NotExist, FsrmPropertyConditionType_PrefixOf, FsrmPropertyConditionType_StartWith, FsrmPropertyConditionType_SuffixOf, FsrmPropertyConditionType_Unknown, fs.fsrmpropertyconditiontype, fsrm.fsrmpropertyconditiontype, fsrm/FsrmPropertyConditionType, fsrm/FsrmPropertyConditionType_Contain, fsrm/FsrmPropertyConditionType_ContainedIn, fsrm/FsrmPropertyConditionType_EndWith, fsrm/FsrmPropertyConditionType_Equal, fsrm/FsrmPropertyConditionType_Exist, fsrm/FsrmPropertyConditionType_GreaterThan, fsrm/FsrmPropertyConditionType_LessThan, fsrm/FsrmPropertyConditionType_MatchesPattern, fsrm/FsrmPropertyConditionType_NotEqual, fsrm/FsrmPropertyConditionType_NotExist, fsrm/FsrmPropertyConditionType_PrefixOf, fsrm/FsrmPropertyConditionType_StartWith, fsrm/FsrmPropertyConditionType_SuffixOf, fsrm/FsrmPropertyConditionType_Unknown
f1_keywords:
- fsrmenums/FsrmPropertyConditionType
dev_langs:
- c++
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h, Fsrmenums.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmEnums.idl
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
- Fsrm.h
api_name:
- FsrmPropertyConditionType
targetos: Windows
req.typenames: FsrmPropertyConditionType
req.redist: 
ms.custom: 19H1
---

# FsrmPropertyConditionType enumeration


## -description


Defines the possible comparison operations that can be used to determine whether a property value of a 
    file meets a particular condition.


## -enum-fields




### -field FsrmPropertyConditionType_Unknown

The operator is unknown; do not use this value.


### -field FsrmPropertyConditionType_Equal

The property condition is met if the property value is equal to a specified value.


### -field FsrmPropertyConditionType_NotEqual

The property condition is met if the property value is not equal to a specified value.


### -field FsrmPropertyConditionType_GreaterThan

The property condition is met if the property value is greater than a specified value.


### -field FsrmPropertyConditionType_LessThan

The property condition is met if the property value is less than a specified value.


### -field FsrmPropertyConditionType_Contain

The property condition is met if the property value contains the specified value.


### -field FsrmPropertyConditionType_Exist

The property condition is met if the property value exists.


### -field FsrmPropertyConditionType_NotExist

The property condition is met if the property value does not exist.


### -field FsrmPropertyConditionType_StartWith

The property condition is met if the property value starts with the specified value.


### -field FsrmPropertyConditionType_EndWith

The property condition is met if the property value ends with the specified value.


### -field FsrmPropertyConditionType_ContainedIn

The property condition is met if the property value is contained in the specified value.


### -field FsrmPropertyConditionType_PrefixOf

The property condition is met if the property value is a prefix of the specified value.


### -field FsrmPropertyConditionType_SuffixOf

The property condition is met if the property value is a suffix of the specified value.


### -field FsrmPropertyConditionType_MatchesPattern

The property condition is met if the property value matches the specified pattern. The pattern format is a 
       semicolon-separated list of wildcard patterns. For example "*.exe;*.com"

<b>Windows Server 2008 R2:  </b>This enumeration value is not supported before Windows Server 2012.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-enumerations">FSRM Enumerations</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfileconditionproperty-get_operator">IFsrmFileConditionProperty.Operator</a>



[IFsrmPropertyCondition.Type](/windows/win32/api/fsrmreports/nf-fsrmreports-ifsrmpropertycondition-get_type)
 

 

