---
UID: NF:wldp.WldpGetApplicationSettingStringSet
tech.root: security
title: WldpGetApplicationSettingStringSet
ms.date: 10/21/2024
targetos: Windows
description: Queries the values of the application setting defined as type `stringset` across all Application Control for Business policies in the supplied file.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: wldp.dll
req.header: wldp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: wldp.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11, Build 26100
req.target-min-winversvr: Windows 11, Build 26100
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - wldp.dll
api_name:
 - WldpGetApplicationSettingStringSet
f1_keywords:
 - WldpGetApplicationSettingStringSet
 - wldp/WldpGetApplicationSettingStringSet
dev_langs:
 - c++
helpviewer_keywords:
 - WldpGetApplicationSettingStringSet
---

## -description

Queries the values of the application setting defined as type `stringset` across all Application Control for Business policies in the supplied file.

Application settings provide Application Control customers with the ability to configure application-defined behvaiors when Application Control is enabled on systems. Software vendors pre-define the settings in manifests, and the behavior in their applications. Application Control provides the reconciled value of those settings from all policies on the system to the calling process. For example, script hosts can allow App Control customers to define whether the buffer, file or stream that failed policy should run in a sandbox or be blocked from executing. App Control defers the definition of application settings to the software vendors and returns the application setting results to the application to handle the behavior. 

## -syntax

```c++
STDAPI
WldpGetApplicationSettingStringSet(
    _In_ PCWSTR Id, 
    _In_ PCWSTR Setting, 
    _In_ SIZE_T DataCount, 
    _Out_ SIZE_T *RequiredCount, 
    _Out_writes_to_opt_(*DataCount, *RequiredCount) PZZWSTR Data 
    );
```

## -parameters

### -param id [in]

A string specifying the application to which the application setting applies.

### -param Setting [in]

A string specifying the name of the setting for which to check all Application Control policies. 

### -param DataCount [in, optional]

A pointer to the size required for the string list `result`, Data. 

### -param RequiredCount [out]

On return, RequiredCount will be populated with the required size of the `result` string, Data. 


### -param Data [out]

Data contains a packed and null-terminated array of null-terminated strings of size *RequiredCount. Callers can unpack the array into a collection of their choise. 

## -returns

Returns S_OK on success and a failure code otherwise.

## -remarks

Within an Application Control policy group, a base policy and its supplemental policies, the values (case insenstitive) for the application setting are unioned together. The results from each policy group are then intersected together and returned. Any policy which does not specify a value for the given application setting is assumed to have an empty set as the value. The results array will not contain any duplicate values. 

Callers should follow the methodology described in [Retrieving Data of Unknown Length](/windows/win32/seccrypto/retrieving-data-of-unknown-length) to properly size the Data buffer. 

## -see-also

- [WldpGetApplicationSettingStringList](nf-wldp-wldpgetapplicationsettingstringlist.md)
- [WldpGetApplicationSettingBoolean](nf-wldp-wldpgetapplicationsettingboolean.md)