---
UID: NE:wbemcli.tag_WBEM_COMPARISON_FLAG
title: tag_WBEM_COMPARISON_FLAG
author: windows-sdk-content
description: Contains flags that define the comparison to perform when using the IWbemClassObject::CompareTo method.
old-location: wmi\wbem_comparison_flag.htm
tech.root: WmiSdk
ms.assetid: B32685D3-C096-4E1F-BF59-EB68ED497FEC
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: WBEM_COMPARISON_FLAG, WBEM_COMPARISON_FLAG enumeration [Windows Management Instrumentation], WBEM_COMPARISON_INCLUDE_ALL, WBEM_FLAG_IGNORE_CASE, WBEM_FLAG_IGNORE_CLASS, WBEM_FLAG_IGNORE_DEFAULT_VALUES, WBEM_FLAG_IGNORE_FLAVOR, WBEM_FLAG_IGNORE_OBJECT_SOURCE, WBEM_FLAG_IGNORE_QUALIFIERS, tag_WBEM_COMPARISON_FLAG, wbemcli/WBEM_COMPARISON_FLAG, wbemcli/WBEM_COMPARISON_INCLUDE_ALL, wbemcli/WBEM_FLAG_IGNORE_CASE, wbemcli/WBEM_FLAG_IGNORE_CLASS, wbemcli/WBEM_FLAG_IGNORE_DEFAULT_VALUES, wbemcli/WBEM_FLAG_IGNORE_FLAVOR, wbemcli/WBEM_FLAG_IGNORE_OBJECT_SOURCE, wbemcli/WBEM_FLAG_IGNORE_QUALIFIERS, wmi.wbem_comparison_flag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemcli.h
api_name:
 - WBEM_COMPARISON_FLAG
product: Windows
targetos: Windows
req.typenames: WBEM_COMPARISON_FLAG
req.redist: 
---

# tag_WBEM_COMPARISON_FLAG enumeration


## -description


Contains flags that define the comparison to perform when using the <a href="https://msdn.microsoft.com/246e5c2e-8d89-4ab5-b9ae-21a41eefa2e2">IWbemClassObject::CompareTo</a> method.


## -enum-fields




### -field WBEM_COMPARISON_INCLUDE_ALL

Compare all features.


### -field WBEM_FLAG_IGNORE_QUALIFIERS

Ignore all qualifiers (including <b>Key</b> and <b>Dynamic</b>) in comparison.


### -field WBEM_FLAG_IGNORE_OBJECT_SOURCE

Ignore the source of the objects, namely the server and the namespace they came from, in comparison to other objects.


### -field WBEM_FLAG_IGNORE_DEFAULT_VALUES

Ignore default values of properties. This flag is only meaningful when comparing classes.


### -field WBEM_FLAG_IGNORE_CLASS

Assume that the objects being compared are instances of the same class. Consequently, this flag compares instance-related information only. Use this flag to optimize performance. If the objects are not of the same class, the results are undefined.


### -field WBEM_FLAG_IGNORE_CASE

Compare string values in a case-insensitive manner. This applies both to strings and to qualifier values. Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.


### -field WBEM_FLAG_IGNORE_FLAVOR

Ignore qualifier flavors. This flag still takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions (for more information, see 
<a href="https://msdn.microsoft.com/6a0769ac-e16c-45e1-92b6-26e4969bf23d">Qualifier Flavors</a>).

