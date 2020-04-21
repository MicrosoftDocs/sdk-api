---
UID: NE:wbemdisp.WbemComparisonFlagEnum
title: WbemComparisonFlagEnum (wbemdisp.h)
description: Define the settings for object comparison and are used by SWbemObject.CompareTo_.helpviewer_keywords: ["WbemComparisonFlagEnum","WbemComparisonFlagEnum enumeration [Windows Management Instrumentation]","_hmm_wbemcomparisonflagenum","wbemComparisonFlagIgnoreCase","wbemComparisonFlagIgnoreClass","wbemComparisonFlagIgnoreDefaultValues","wbemComparisonFlagIgnoreFlavor","wbemComparisonFlagIgnoreObjectSource","wbemComparisonFlagIgnoreQualifiers","wbemComparisonFlagIncludeAll","wbemdisp/WbemComparisonFlagEnum","wbemdisp/wbemComparisonFlagIgnoreCase","wbemdisp/wbemComparisonFlagIgnoreClass","wbemdisp/wbemComparisonFlagIgnoreDefaultValues","wbemdisp/wbemComparisonFlagIgnoreFlavor","wbemdisp/wbemComparisonFlagIgnoreObjectSource","wbemdisp/wbemComparisonFlagIgnoreQualifiers","wbemdisp/wbemComparisonFlagIncludeAll","wmi.wbemcomparisonflagenum"]
old-location: wmi\wbemcomparisonflagenum.htm
tech.root: WmiSdk
ms.assetid: 83fda164-1e98-499b-b599-f999e69ad501
ms.date: 12/05/2018
ms.keywords: WbemComparisonFlagEnum, WbemComparisonFlagEnum enumeration [Windows Management Instrumentation], _hmm_wbemcomparisonflagenum, wbemComparisonFlagIgnoreCase, wbemComparisonFlagIgnoreClass, wbemComparisonFlagIgnoreDefaultValues, wbemComparisonFlagIgnoreFlavor, wbemComparisonFlagIgnoreObjectSource, wbemComparisonFlagIgnoreQualifiers, wbemComparisonFlagIncludeAll, wbemdisp/WbemComparisonFlagEnum, wbemdisp/wbemComparisonFlagIgnoreCase, wbemdisp/wbemComparisonFlagIgnoreClass, wbemdisp/wbemComparisonFlagIgnoreDefaultValues, wbemdisp/wbemComparisonFlagIgnoreFlavor, wbemdisp/wbemComparisonFlagIgnoreObjectSource, wbemdisp/wbemComparisonFlagIgnoreQualifiers, wbemdisp/wbemComparisonFlagIncludeAll, wmi.wbemcomparisonflagenum
f1_keywords:
- wbemdisp/WbemComparisonFlagEnum
dev_langs:
- c++
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wbemdisp.idl
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
- Wbemdisp.h
api_name:
- WbemComparisonFlagEnum
targetos: Windows
req.typenames: WbemComparisonFlagEnum
req.redist: 
ms.custom: 19H1
---

# WbemComparisonFlagEnum enumeration


## -description


The 
WbemComparisonFlagEnum constants define the settings for object comparison and are used by 
<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/swbemobject-compareto-">SWbemObject.CompareTo_</a>.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library; script languages must use the value of the constant directly, unless they use the Windows Script Host (WSH) XML file format. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library">Using the WMI Scripting Type Library</a>.


## -enum-fields




### -field wbemComparisonFlagIncludeAll

Used to compare all properties, qualifiers, and flavors.


### -field wbemComparisonFlagIgnoreQualifiers

Ignores all qualifiers (including <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/key-qualifier">Key</a> and <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/standard-wmi-qualifiers">Dynamic</a>) in comparison.


### -field wbemComparisonFlagIgnoreObjectSource

Ignores the source of the objects, namely the server and the namespace they came from, in comparison to other objects.


### -field wbemComparisonFlagIgnoreDefaultValues

Ignores default values of properties (only meaningful when comparing classes).


### -field wbemComparisonFlagIgnoreClass

Instructs the system to assume that the objects being compared are instances of the same class. Consequently, this constant compares instance-related information only. Use to optimize performance. If the objects are not of the same class, the results will be undefined.


### -field wbemComparisonFlagIgnoreCase

Compares string values in a case-insensitive manner. This applies both to strings and to qualifier values. Property and qualifier names are always compared in a case-insensitive manner whether this constant is specified or not.


### -field wbemComparisonFlagIgnoreFlavor

Ignore qualifier flavors. This constant still takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/scripting-api-constants">Scripting API Constants</a>
 

 

