---
UID: NF:propvarutil.PropVariantToUInt64WithDefault
title: PropVariantToUInt64WithDefault function
author: windows-sdk-content
description: Extracts ULONGLONG value from a PROPVARIANT structure. If no value exists, then the specified default value is returned.
old-location: properties\PropVariantToUInt64WithDefault.htm
old-project: properties
ms.assetid: 8ca0e25e-6a3f-41ff-9a4a-7cca9a02d07c
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PropVariantToUInt64WithDefault, PropVariantToUInt64WithDefault function [Windows Properties], properties.PropVariantToUInt64WithDefault, propvarutil/PropVariantToUInt64WithDefault, shell.PropVariantToUInt64WithDefault, shell_PropVariantToUInt64WithDefault
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PropVariantToUInt64WithDefault
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# PropVariantToUInt64WithDefault function


## -description


Extracts <b>ULONGLONG</b> value from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. If no value exists, then the specified default value is returned.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param ullDefault [in]

Type: <b>ULONGLONG</b>

Specifies a default property value, for use where no value currently exists.


## -returns



Type: <b>ULONGLONG</b>

Returns the extracted unsigned <b>LONGLONG</b> value, or a default.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a <b>ULONGLONG</b> value and would like to use a default value if it does not. For instance, an application obtaining values from a property store can use this to safely extract the <b>ULONGLONG</b> value for <b>UInt64</b> properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_UI8</b>, this helper function extracts the <b>ULONGLONG</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>ULONGLONG</b>. If the source <b>PROPVARIANT</b> has type <b>VT_EMPTY</b> or a conversion is not possible, then <a href="shell.PropVariantToUInt64WithDefault">PropVariantToUInt64WithDefault</a> will return the default provided by <i>ullDefault</i>. See <a href="shell.PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PropVariantToUInt64WithDefault">PropVariantToUInt64WithDefault</a> to access a <b>ULONGLONG</b> value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore-&gt;GetValue(PKEY_Size, &amp;propvar);
if (SUCCEEDED(hr))
{
     // PKEY_Size is expected to produce a VT_UI8 or VT_EMPTY value.
     // The application developer decided to treat VT_EMPTY or invalid values as 0
     ULONGLONG ullSize = PropVariantToUInt64WithDefault(propvar, 0);
     // ullSize is now valid.
     PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>


