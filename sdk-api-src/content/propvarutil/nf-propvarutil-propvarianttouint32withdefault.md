---
UID: NF:propvarutil.PropVariantToUInt32WithDefault
title: PropVariantToUInt32WithDefault function
author: windows-sdk-content
description: Extracts a ULONG value from a PROPVARIANT structure. If no value exists, then a specified default value is returned.
old-location: properties\PropVariantToUInt32WithDefault.htm
tech.root: properties
ms.assetid: 8ace8c3f-fea2-4b20-9e0b-3abfbd569b54
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PropVariantToUInt32WithDefault, PropVariantToUInt32WithDefault function [Windows Properties], properties.PropVariantToUInt32WithDefault, propvarutil/PropVariantToUInt32WithDefault, shell.PropVariantToUInt32WithDefault, shell_PropVariantToUInt32WithDefault
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
 - PropVariantToUInt32WithDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantToUInt32WithDefault function


## -description


Extracts a <b>ULONG</b> value from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. If no value exists, then a specified default value is returned.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param ulDefault [in]

Type: <b>ULONG</b>

Specifies a default property value, for use where no value currently exists.


## -returns



Type: <b>ULONG</b>

Returns extracted <b>ULONG</b> value, or default.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a <b>ULONG</b> value and would like to use a default value if it does not. For instance, an application obtaining values from a property store can use this to safely extract the <b>ULONG</b> value for <b>UInt32</b> properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_UI4</b>, this helper function extracts the <b>ULONG</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>ULONG</b>. If the source <b>PROPVARIANT</b> has type <b>VT_EMPTY</b> or a conversion is not possible, then <a href="shell.PropVariantToUInt32WithDefault">PropVariantToUInt32WithDefault</a> will return the default provided by <i>ulDefault</i>. See <a href="shell.PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PropVariantToUInt32WithDefault">PropVariantToUInt32WithDefault</a> to access a <b>ULONG</b> value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore-&gt;GetValue(PKEY_Rating, &amp;propvar);
if (SUCCEEDED(hr))
{
     // PKEY_Rating is expected to produce a VT_UI4 or VT_EMPTY value.
     // The application developer decided to treat VT_EMPTY or invalid values as 0
     ULONG uRating = PropVariantToUInt32WithDefault(propvar, 0);
     // uRating is now valid.
     PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromUInt32">InitPropVariantFromUInt32</a>



<a href="shell.PropVariantChangeType">PropVariantChangeType</a>



<a href="shell.PropVariantToUInt32">PropVariantToUInt32</a>



<a href="shell.VariantToUInt32">VariantToUInt32</a>
 

 

