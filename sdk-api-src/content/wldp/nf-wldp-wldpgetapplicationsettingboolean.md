---
UID: NF:wldp.WldpGetApplicationSettingBoolean
tech.root: security
title: WldpGetApplicationSettingBoolean
ms.date: 10/21/2024
targetos: Windows
description: Queries the values of the application setting defined as type `boolean` across all Application Control for Business policies in the supplied file.
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
 - WldpGetApplicationSettingBoolean
f1_keywords:
 - WldpGetApplicationSettingBoolean
 - wldp/WldpGetApplicationSettingBoolean
dev_langs:
 - c++
helpviewer_keywords:
 - WldpGetApplicationSettingBoolean
---

## -description

Queries the values of the application setting defined as type `boolean` across all Application Control for Business policies in the supplied file.

Application settings provide Application Control customers with the ability to configure application-defined behvaiors when Application Control is enabled on systems. Software vendors pre-define the settings in manifests, and the behavior in their applications. Application Control provides the reconciled value of those settings from all policies on the system to the calling process. For example, script hosts can allow App Control customers to define whether the buffer, file or stream that failed policy should run in a sandbox or be blocked from executing. App Control defers the definition of application settings to the software vendors and returns the application setting results to the application to handle the behavior. 

## -syntax

```c++
STDAPI
WldpGetApplicationSettingBoolean(
    _In_ PCWSTR Id, 
    _In_ PCWSTR Setting, 
    _Out_ BOOL_ *Result, 
    );
```

## -parameters

### -param id [in]

A string specifying the application to which the application setting applies.

### -param Setting [in]

A string specifying the name of the setting for which to check all Application Control policies. 

### -param Result [out]

Contains a. The data should be interpreted as: 

- `1` being a `true` value for the application setting
- `0` being a `false` value for the application setting

## -returns

Returns S_OK on success and a failure code otherwise.

## -remarks

Within an Application Control policy group, a base policy and its supplemental policies, the boolean values for the application setting are unioned together. The results from each policy group are then intersected together and returned. Any policy which does not specify a value for the given application setting is assumed to have the value `false`.  

## -see-also

- [WldpGetApplicationSettingStringList](nf-wldp-wldpgetapplicationsettingstringlist.md)
- [WldpGetApplicationSettingStringSet](nf-wldp-wldpgetapplicationsettingstringset.md)