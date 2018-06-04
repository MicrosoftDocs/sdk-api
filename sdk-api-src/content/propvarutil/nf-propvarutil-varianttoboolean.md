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

# VariantToBoolean function


## -description


Extracts the value of a Boolean property from a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure. If no value can be extracted, then a default value is assigned.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


### -param pfRet [out]

Type: <b>BOOL*</b>

When this function returns, contains the extracted value if one exists; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used when the calling application expects a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> to hold a Boolean value. For instance, an application that obtains values from a Shell folder can use this function to safely extract the value from one of the folder's Boolean properties.

If the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> is of type VT_BOOL, this function extracts the <b>BOOL</b> value.

If the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> is not of type VT_BOOL, this function attempts to convert the value in the <b>VARIANT</b> structure into a <b>BOOL</b>. If a conversion is not possible, <a href="shell.VariantToBoolean">VariantToBoolean</a> returns a failure code and sets <i>pfRet</i> to <b>FALSE</b>. See <a href="shell.PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions. Of note, VT_EMPTY is successfully converted to <b>FALSE</b>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.VariantToBoolean">VariantToBoolean</a> to access a <b>BOOL</b> value in a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// VARIANT var;
// Assume variable var is initialize and valid. 
// The application expects it to hold a VT_BOOL value.
BOOL fValue;

HRESULT hr = VariantToBoolean(var, &amp;fValue);

if (SUCCEEDED(hr))
{
    // fValue is now valid.
}
else
{
    // fValue is always FALSE.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitVariantFromBoolean">InitVariantFromBoolean</a>



<a href="shell.PropVariantChangeType">PropVariantChangeType</a>



<a href="shell.PropVariantToBoolean">PropVariantToBoolean</a>



<a href="shell.VariantToBooleanArray">VariantToBooleanArray</a>
 

 

