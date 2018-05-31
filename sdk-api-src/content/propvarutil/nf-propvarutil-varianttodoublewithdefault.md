---
UID: NF:propvarutil.VariantToDoubleWithDefault
title: VariantToDoubleWithDefault function
author: windows-sdk-content
description: Extracts a DOUBLE value from a VARIANT structure. If no value exists, then the specified default value is returned.
old-location: properties\VariantToDoubleWithDefault.htm
old-project: properties
ms.assetid: a3e32a30-363d-487e-bdd5-ac2616d6de14
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: VariantToDoubleWithDefault, VariantToDoubleWithDefault function [Windows Properties], _shell_VariantToDoubleWithDefault, properties.VariantToDoubleWithDefault, propvarutil/VariantToDoubleWithDefault, shell.VariantToDoubleWithDefault
ms.prod: windows
ms.technology: windows-sdk
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
-	VariantToDoubleWithDefault
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# VariantToDoubleWithDefault function


## -description


Extracts a <b>DOUBLE</b> value from a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure. If no value exists, then the specified default value is returned.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


### -param dblDefault [in]

Type: <b>DOUBLE</b>

The default value for use where no extractable value exists.


## -returns



Type: <b>DOUBLE</b>

Returns the extracted <b>double</b> value; otherwise, the default value specified in <i>dblDefault</i>.




## -remarks



This helper function is used when the calling application expects a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> to hold a <b>DOUBLE</b> value and wants to use a default value if it does not.

If the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> is of type VT_R8, this helper extracts the <b>DOUBLE</b> value.

If the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> is not of type VT_R8, the function attempts to convert the value in the <b>VARIANT</b> into a <b>DOUBLE</b>.

If the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> is of type VT_EMPTY or a conversion is not possible, then <a href="shell.VariantToDoubleWithDefault">VariantToDoubleWithDefault</a> returns the default value provided by <i>dblDefault</i>. See <a href="shell.PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.VariantToDoubleWithDefault">VariantToDoubleWithDefault</a> to access a <b>DOUBLE</b> value stored in a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// VARIANT var;
// Assume variable var is initialized and valid.
// The application expects var to hold a DOUBLE value.

// The application wants to treat VT_EMPTY as 3.1415.
DOUBLE dblValue = VariantToDoubleWithDefault(var, 3.1415);

// dblValue is now valid.</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitVariantFromDouble">InitVariantFromDouble</a>



<a href="shell.PropVariantChangeType">PropVariantChangeType</a>



<a href="shell.PropVariantToDouble">PropVariantToDouble</a>



<a href="shell.VariantToDouble">VariantToDouble</a>
 

 

