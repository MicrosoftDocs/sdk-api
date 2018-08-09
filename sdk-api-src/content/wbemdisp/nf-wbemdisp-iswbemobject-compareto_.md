---
UID: NF:wbemdisp.ISWbemObject.CompareTo_
title: ISWbemObject::CompareTo_
author: windows-sdk-content
description: The CompareTo_ method of the SWbemObject object compares two SWbemObject objects. This comparison is subject to certain constraints based on the values specified in the iFlags parameter.
old-location: wmi\swbemobject_compareto_.htm
old-project: WmiSdk
ms.assetid: 38813551-2403-4def-ae57-2b17f72cd180
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CompareTo_, CompareTo_ method [Windows Management Instrumentation], CompareTo_ method [Windows Management Instrumentation],ISWbemObject interface, CompareTo_ method [Windows Management Instrumentation],SWbemObject object, ISWbemObject interface [Windows Management Instrumentation],CompareTo_ method, ISWbemObject.CompareTo_, ISWbemObject::CompareTo_, SWbemObject object [Windows Management Instrumentation],CompareTo_ method, SWbemObject.CompareTo_, _hmm_swbemobject.compareto_, wbemComparisonFlagIgnoreCase, wbemComparisonFlagIgnoreClass, wbemComparisonFlagIgnoreDefaultValues, wbemComparisonFlagIgnoreFlavor, wbemComparisonFlagIgnoreObjectSource, wbemComparisonFlagIgnoreQualifiers, wbemComparisonFlagIncludeAll, wmi.swbemobject_compareto_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
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
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemObject.CompareTo_
 - ISWbemObject.CompareTo_
 - ISWbemObject.CompareTo_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::CompareTo_


## -description


The 
<b>CompareTo_</b> method of the 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object compares two <b>SWbemObject</b> objects. This comparison is subject to certain constraints based on the values specified in the <i>iFlags</i> parameter.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemObject




### -param iFlags [in, optional]

Specifies the object characteristics to consider when comparing an object with other objects. You can use <b>wbemComparisonFlagIncludeAll</b> to consider all features (this is the default), or any combination of the following values.



#### wbemComparisonFlagIncludeAll (0 (0x0))

Compares all properties, qualifiers, and flavors.



#### wbemComparisonFlagIgnoreObjectSource (2 (0x2))

Causes the source of the objects, namely the server and the namespace they came from, to be ignored in comparison to other objects.



#### wbemComparisonFlagIgnoreQualifiers (1 (0x1))

Causes all qualifiers (including <b>Key</b> and <b>Dynamic</b>) to be ignored in comparison.



#### wbemComparisonFlagIgnoreDefaultValues (4 (0x4))

Causes default values of properties to be ignored. This flag is only meaningful when comparing classes.



#### wbemComparisonFlagIgnoreFlavor (32 (0x20))

Causes qualifier flavors to be ignored. This flag takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.



#### wbemComparisonFlagIgnoreCase (16 (0x10))

Compares string values in a case-insensitive manner. This applies both to strings and to qualifier values. Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.



#### wbemComparisonFlagIgnoreClass (8 (0x8))

Instructs the system to assume that the objects being compared are instances of the same class. Consequently, this flag compares instance-related information only. Use this flag to optimize performance. If the objects are not of the same class, the results are undefined.


### -param bResult






#### - objwbemObject [in]

Required. This parameter is an 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object. This is the object with which the first object is compared. The object must be a valid <b>SWbemObject</b> instance.


## -returns



This method returns the Boolean value of <b>TRUE</b> if the objects match. It returns <b>FALSE</b> if the objects do not match.




## -see-also




<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>
 

 

