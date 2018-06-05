---
UID: NF:propvarutil.InitPropVariantFromUInt16
title: InitPropVariantFromUInt16 function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a 16-bit unsigned integer value.
old-location: properties\InitPropVariantFromUInt16.htm
old-project: properties
ms.assetid: 2f4b0c6b-2d68-4ea6-a7fb-7884071dcfbe
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: InitPropVariantFromUInt16, InitPropVariantFromUInt16 function [Windows Properties], properties.InitPropVariantFromUInt16, propvarutil/InitPropVariantFromUInt16, shell.InitPropVariantFromUInt16, shell_InitPropVariantFromUInt16
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
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Propvarutil.h
api_name:
-	InitPropVariantFromUInt16
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# InitPropVariantFromUInt16 function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a 16-bit unsigned integer value.


## -parameters




### -param uiVal [in]

Type: <b>USHORT</b>

Source value.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_UI2 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantFromUInt16">InitPropVariantFromUInt16</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromUInt16(5, &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_UI2.
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitVariantFromUInt16">InitVariantFromUInt16</a>



<a href="shell.PropVariantToUInt16">PropVariantToUInt16</a>



<a href="shell.PropVariantToUInt16WithDefault">PropVariantToUInt16WithDefault</a>
 

 

