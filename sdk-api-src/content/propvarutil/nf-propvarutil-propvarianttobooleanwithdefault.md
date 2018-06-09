---
UID: NF:propvarutil.PropVariantToBooleanWithDefault
title: PropVariantToBooleanWithDefault function
author: windows-sdk-content
description: Extracts the Boolean property value of a PROPVARIANT structure. If no value exists, then the specified default value is returned.
old-location: properties\PropVariantToBooleanWithDefault.htm
old-project: properties
ms.assetid: 223767a7-a4de-4e7e-ad8b-2a6bdcea0a47
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PropVariantToBooleanWithDefault, PropVariantToBooleanWithDefault function [Windows Properties], properties.PropVariantToBooleanWithDefault, propvarutil/PropVariantToBooleanWithDefault, shell.PropVariantToBooleanWithDefault, shell_PropVariantToBooleanWithDefault
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
 - PropVariantToBooleanWithDefault
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PropVariantToBooleanWithDefault function


## -description


Extracts the Boolean property value of a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. If no value exists, then the specified default value is returned.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param fDefault [in]

Type: <b>BOOL</b>

Specifies the default property value, for use where no value currently exists.


## -returns



Type: <b>BOOL</b>

The extracted Boolean value or the default value.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a Boolean value and would like to use a default value if it does not. For instance, an application that obtains values from a property store can use this to safely extract the Boolean value for Boolean properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_BOOL</b>, this helper function extracts the Boolean value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a Boolean. If the source <b>PROPVARIANT</b> has type <b>VT_EMPTY</b> or a conversion is not possible, then <a href="https://www.bing.com/search?q=PropVariantToBooleanWithDefault">PropVariantToBooleanWithDefault</a> returns the default provided by <i>fDefault</i>. See <a href="https://www.bing.com/search?q=PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://www.bing.com/search?q=PropVariantToBooleanWithDefault">PropVariantToBooleanWithDefault</a> to access a Boolean value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;
// Assume the variable ppropstore is initialized and valid.
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore-&gt;GetValue(PKEY_IsRead, &amp;propvar);

if (SUCCEEDED(hr))
{
     // PKEY_IsRead is expected to produce a VT_BOOL or VT_EMPTY value.
     // The application developer decided to treat VT_EMPTY or invalid values as TRUE
     BOOL fShared = PropVariantToBooleanWithDefault(propvar, TRUE);
     
     // fShared is now valid.
     PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>


