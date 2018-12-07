---
UID: NF:propvarutil.PropVariantCompareEx
title: PropVariantCompareEx function
author: windows-sdk-content
description: Extends PropVariantCompare by allowing the caller to compare two PROPVARIANT structures based on specified comparison units and flags.
old-location: properties\PropVariantCompareEx.htm
tech.root: properties
ms.assetid: 0fc9eb7b-e981-430c-b50e-77eb51620a76
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PVCF_DEFAULT, PVCF_TREATEMPTYASGREATERTHAN, PVCF_USESTRCMP, PVCF_USESTRCMPC, PVCF_USESTRCMPI, PVCF_USESTRCMPIC, PropVariantCompareEx, PropVariantCompareEx function [Windows Properties], _shell_PropVariantCompareEx, properties.PropVariantCompareEx, propvarutil/PropVariantCompareEx, shell.PropVariantCompareEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PropVariantCompareEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantCompareEx function


## -description


Extends <a href="https://msdn.microsoft.com/en-us/library/Bb776516(v=VS.85).aspx">PropVariantCompare</a> by allowing the caller to compare two <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures based on specified comparison units and flags.


## -parameters




### -param propvar1 [in]

Type: <b>REFPROPVARIANT</b>

Reference to the first <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param propvar2 [in]

Type: <b>REFPROPVARIANT</b>

Reference to the second <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param unit [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb762530(v=VS.85).aspx">PROPVAR_COMPARE_UNIT</a></b>

Specifies, where appropriate, one of the comparison units defined in <a href="https://msdn.microsoft.com/en-us/library/Bb762530(v=VS.85).aspx">PROPVAR_COMPARE_UNIT</a>.


### -param flags [in]

Type: <b>PROPVAR_COMPARE_FLAGS</b>

Specifies one of the following:



#### PVCF_DEFAULT (0x00000000)

When comparing strings, use <a href="https://msdn.microsoft.com/013c6db3-7d14-44ef-89af-b3aac28f4e3f">StrCmpLogical</a>.



#### PVCF_TREATEMPTYASGREATERTHAN (0x00000001)

Regard empty or null values as greater than non-empty values. This value can be OR-ed with any other value.



#### PVCF_USESTRCMP (0x00000002)

When comparing strings, use <a href="https://msdn.microsoft.com/12530a04-776c-4506-86d1-07e2c3569a36">StrCmp</a>.



#### PVCF_USESTRCMPC (0x00000004)

When comparing strings, use <a href="https://msdn.microsoft.com/f4c4bc76-1e42-4cb0-bf74-d395743c9b1c">StrCmpC</a>.



#### PVCF_USESTRCMPI (0x00000008)

When comparing strings, use <a href="https://msdn.microsoft.com/d059b6bd-8f03-4273-aa7a-b8b07f84d268">StrCmpI</a>.



#### PVCF_USESTRCMPIC (0x00000010)

When comparing strings, use <a href="https://msdn.microsoft.com/3f6d1ca1-fbd2-4ce2-b6d4-c3dfb37f1f87">StrCmpIC</a>.


## -returns



Type: <b>INT</b>

<ul>
<li>Returns 1 if <i>propvar1</i> is greater than <i>propvar2</i></li>
<li>Returns 0 if <i>propvar1</i> equals <i>propvar2</i></li>
<li>Returns -1 if <i>propvar1</i> is less than <i>propvar2</i></li>
</ul>



## -remarks



This function does not compare all types; only selected types are currently comparable.

By default, VT_NULL / VT_EMPTY / 0-element vectors are considered to be less than any other vartype.

If the vartypes are different, this function attempts to convert <i>propvar2</i> to the vartype of <i>propvar1</i> before comparing them.

<div class="alert"><b>Note</b>  Behavior of this function, and therefore the results it returns, can change from release to release. It should not be used for canonical sorting applications.</div>
<div> </div>


