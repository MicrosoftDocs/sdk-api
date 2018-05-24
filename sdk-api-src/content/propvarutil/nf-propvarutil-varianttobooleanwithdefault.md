---
UID: NF:propvarutil.VariantToBooleanWithDefault
title: VariantToBooleanWithDefault function
author: windows-driver-content
description: Extracts a BOOL value from a VARIANT structure. If no value exists, then the specified default value is returned.
old-location: properties\VariantToBooleanWithDefault.htm
old-project: properties
ms.assetid: 523c6e75-a51c-4ef7-928c-0d228ab0d337
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: VariantToBooleanWithDefault, VariantToBooleanWithDefault function [Windows Properties], _shell_VariantToBooleanWithDefault, properties.VariantToBooleanWithDefault, propvarutil/VariantToBooleanWithDefault, shell.VariantToBooleanWithDefault
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	VariantToBooleanWithDefault
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# VariantToBooleanWithDefault function


## -description


Extracts a <b>BOOL</b> value from a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure. If no value exists, then the specified default value is returned.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


### -param fDefault [in]

Type: <b>BOOL</b>

The default value for use where no extractable value exists.


## -returns



Type: <b>BOOL</b>

Returns the extracted <b>BOOL</b> value; otherwise, the default value specified in <i>fDefault</i>.




## -remarks



This helper function is used when the calling application expects a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> to hold a <b>BOOL</b> value and wants to use a default value if it does not.

If the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> is of type VT_BOOL, this helper extracts the <b>BOOL</b> value.

If the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> is not of type VT_BOOL, the function attempts to convert the value in the <b>VARIANT</b> into a <b>BOOL</b>.

If the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> is of type VT_EMPTY or a conversion is not possible, then <a href="shell.VariantToBooleanWithDefault">VariantToBooleanWithDefault</a> returns the default value provided by <i>fDefault</i>. See <a href="shell.PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.VariantToBooleanWithDefault">VariantToBooleanWithDefault</a> to access a <b>BOOL</b> value stored in a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// VARIANT var;
// Assume variable var is initialized and valid.  
// The application expects var to hold a BOOL value.
// The application treats VT_EMPTY as FALSE.

BOOL fValue = VariantToBooleanWithDefault(var, FALSE);

// fValue is now valid.</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitVariantFromBoolean">InitVariantFromBoolean</a>



<a href="shell.PropVariantChangeType">PropVariantChangeType</a>



<a href="shell.PropVariantToBoolean">PropVariantToBoolean</a>



<a href="shell.VariantToBoolean">VariantToBoolean</a>
 

 

