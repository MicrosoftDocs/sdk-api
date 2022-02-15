---
UID: NE:wbemcli.tag_WBEM_COMPARISON_FLAG
title: WBEM_COMPARISON_FLAG (wbemcli.h)
description: Contains flags that define the comparison to perform when using the IWbemClassObject::CompareTo method.
helpviewer_keywords: ["WBEM_COMPARISON_FLAG","WBEM_COMPARISON_FLAG enumeration [Windows Management Instrumentation]","WBEM_COMPARISON_INCLUDE_ALL","WBEM_FLAG_IGNORE_CASE","WBEM_FLAG_IGNORE_CLASS","WBEM_FLAG_IGNORE_DEFAULT_VALUES","WBEM_FLAG_IGNORE_FLAVOR","WBEM_FLAG_IGNORE_OBJECT_SOURCE","WBEM_FLAG_IGNORE_QUALIFIERS","wbemcli/WBEM_COMPARISON_FLAG","wbemcli/WBEM_COMPARISON_INCLUDE_ALL","wbemcli/WBEM_FLAG_IGNORE_CASE","wbemcli/WBEM_FLAG_IGNORE_CLASS","wbemcli/WBEM_FLAG_IGNORE_DEFAULT_VALUES","wbemcli/WBEM_FLAG_IGNORE_FLAVOR","wbemcli/WBEM_FLAG_IGNORE_OBJECT_SOURCE","wbemcli/WBEM_FLAG_IGNORE_QUALIFIERS","wmi.wbem_comparison_flag"]
old-location: wmi\wbem_comparison_flag.htm
tech.root: wmi
ms.assetid: B32685D3-C096-4E1F-BF59-EB68ED497FEC
ms.date: 12/05/2018
ms.keywords: WBEM_COMPARISON_FLAG, WBEM_COMPARISON_FLAG enumeration [Windows Management Instrumentation], WBEM_COMPARISON_INCLUDE_ALL, WBEM_FLAG_IGNORE_CASE, WBEM_FLAG_IGNORE_CLASS, WBEM_FLAG_IGNORE_DEFAULT_VALUES, WBEM_FLAG_IGNORE_FLAVOR, WBEM_FLAG_IGNORE_OBJECT_SOURCE, WBEM_FLAG_IGNORE_QUALIFIERS, wbemcli/WBEM_COMPARISON_FLAG, wbemcli/WBEM_COMPARISON_INCLUDE_ALL, wbemcli/WBEM_FLAG_IGNORE_CASE, wbemcli/WBEM_FLAG_IGNORE_CLASS, wbemcli/WBEM_FLAG_IGNORE_DEFAULT_VALUES, wbemcli/WBEM_FLAG_IGNORE_FLAVOR, wbemcli/WBEM_FLAG_IGNORE_OBJECT_SOURCE, wbemcli/WBEM_FLAG_IGNORE_QUALIFIERS, wmi.wbem_comparison_flag
req.header: wbemcli.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WBEM_COMPARISON_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_WBEM_COMPARISON_FLAG
 - wbemcli/tag_WBEM_COMPARISON_FLAG
 - WBEM_COMPARISON_FLAG
 - wbemcli/WBEM_COMPARISON_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemcli.h
api_name:
 - WBEM_COMPARISON_FLAG
---

# WBEM_COMPARISON_FLAG enumeration


## -description

Contains flags that define the comparison to perform when using the <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-compareto">IWbemClassObject::CompareTo</a> method.

## -enum-fields

### -field WBEM_COMPARISON_INCLUDE_ALL:0

Compare all features.

### -field WBEM_FLAG_IGNORE_QUALIFIERS:0x1

Ignore all qualifiers (including <b>Key</b> and <b>Dynamic</b>) in comparison.

### -field WBEM_FLAG_IGNORE_OBJECT_SOURCE:0x2

Ignore the source of the objects, namely the server and the namespace they came from, in comparison to other objects.

### -field WBEM_FLAG_IGNORE_DEFAULT_VALUES:0x4

Ignore default values of properties. This flag is only meaningful when comparing classes.

### -field WBEM_FLAG_IGNORE_CLASS:0x8

Assume that the objects being compared are instances of the same class. Consequently, this flag compares instance-related information only. Use this flag to optimize performance. If the objects are not of the same class, the results are undefined.

### -field WBEM_FLAG_IGNORE_CASE:0x10

Compare string values in a case-insensitive manner. This applies both to strings and to qualifier values. Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.

### -field WBEM_FLAG_IGNORE_FLAVOR:0x20

Ignore qualifier flavors. This flag still takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions (for more information, see 
<a href="/windows/desktop/WmiSdk/qualifier-flavors">Qualifier Flavors</a>).
