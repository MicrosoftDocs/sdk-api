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
 

 

