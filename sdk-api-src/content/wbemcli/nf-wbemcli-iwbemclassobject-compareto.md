---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWbemClassObject::CompareTo


## -description


The <b>IWbemClassObject::CompareTo</b> method compares an object to another Windows Management object. Note that there are certain constraints in this comparison process.


## -parameters




### -param lFlags [in]

Specifies the object characteristics to consider in comparison to another object. It can be <b>WBEM_COMPARISON_INCLUDE_ALL</b> to consider all features, or any combination of these flags.



#### WBEM_FLAG_IGNORE_OBJECT_SOURCE

Ignore the source of the objects, namely the server and the namespace they came from, in comparison to other objects.



#### WBEM_FLAG_IGNORE_QUALIFIERS

Ignore all qualifiers (including <b>Key</b> and <b>Dynamic</b>) in comparison.



#### WBEM_FLAG_IGNORE_DEFAULT_VALUES

Ignore default values of properties. This flag is only meaningful when comparing classes.



#### WBEM_FLAG_IGNORE_FLAVOR

Ignore qualifier flavors. This flag still takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions (for more information, see 
<a href="https://msdn.microsoft.com/6a0769ac-e16c-45e1-92b6-26e4969bf23d">Qualifier Flavors</a>).



#### WBEM_FLAG_IGNORE_CASE

Compare string values in a case-insensitive manner. This applies both to strings and to qualifier values. Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.



#### WBEM_FLAG_IGNORE_CLASS

Assume that the objects being compared are instances of the same class. Consequently, this flag compares instance-related information only. Use this flag to optimize performance. If the objects are not of the same class, the results are undefined.


### -param pCompareTo [in]

Object in comparison. This pointer must point to a valid 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> instance. It cannot be <b>NULL</b>.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/6a0769ac-e16c-45e1-92b6-26e4969bf23d">Qualifier Flavors</a>



<a href="https://msdn.microsoft.com/B32685D3-C096-4E1F-BF59-EB68ED497FEC">WBEM_COMPARISON_FLAG</a>
 

 

