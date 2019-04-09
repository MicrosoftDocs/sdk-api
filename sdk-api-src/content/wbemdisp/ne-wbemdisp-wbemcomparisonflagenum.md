---
UID: NE:wbemdisp.WbemComparisonFlagEnum
title: WbemComparisonFlagEnum (wbemdisp.h)
author: windows-sdk-content
description: Define the settings for object comparison and are used by SWbemObject.CompareTo_.
old-location: wmi\wbemcomparisonflagenum.htm
tech.root: WmiSdk
ms.assetid: 83fda164-1e98-499b-b599-f999e69ad501
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WbemComparisonFlagEnum, WbemComparisonFlagEnum enumeration [Windows Management Instrumentation], _hmm_wbemcomparisonflagenum, wbemComparisonFlagIgnoreCase, wbemComparisonFlagIgnoreClass, wbemComparisonFlagIgnoreDefaultValues, wbemComparisonFlagIgnoreFlavor, wbemComparisonFlagIgnoreObjectSource, wbemComparisonFlagIgnoreQualifiers, wbemComparisonFlagIncludeAll, wbemdisp/WbemComparisonFlagEnum, wbemdisp/wbemComparisonFlagIgnoreCase, wbemdisp/wbemComparisonFlagIgnoreClass, wbemdisp/wbemComparisonFlagIgnoreDefaultValues, wbemdisp/wbemComparisonFlagIgnoreFlavor, wbemdisp/wbemComparisonFlagIgnoreObjectSource, wbemdisp/wbemComparisonFlagIgnoreQualifiers, wbemdisp/wbemComparisonFlagIncludeAll, wmi.wbemcomparisonflagenum
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: WbemComparisonFlagEnum
req.redist: 
---

# WbemComparisonFlagEnum enumeration


## -description


The 
WbemComparisonFlagEnum constants define the settings for object comparison and are used by 
<a href="https://msdn.microsoft.com/38813551-2403-4def-ae57-2b17f72cd180">SWbemObject.CompareTo_</a>.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library; script languages must use the value of the constant directly, unless they use the Windows Script Host (WSH) XML file format. For more information, see 
<a href="https://msdn.microsoft.com/6ef4e210-0733-4f2a-89c1-1a7aca5a19d9">Using the WMI Scripting Type Library</a>.


## -enum-fields




### -field wbemComparisonFlagIncludeAll

Used to compare all properties, qualifiers, and flavors.


### -field wbemComparisonFlagIgnoreQualifiers

Ignores all qualifiers (including <a href="https://msdn.microsoft.com/838d295f-e812-4e46-99a4-d2714a0ae8dc">Key</a> and <a href="https://msdn.microsoft.com/63bdbafc-51f3-4714-8b7e-9d5a61cef45e">Dynamic</a>) in comparison.


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




<a href="https://msdn.microsoft.com/feaab757-3167-420b-8f42-edced4cd4c53">Scripting API Constants</a>
 

 

