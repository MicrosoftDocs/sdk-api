---
UID: NF:propvarutil.InitPropVariantFromGUIDAsBuffer
title: InitPropVariantFromGUIDAsBuffer function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a GUID. The structure is initialized as VT_VECTOR | VT_UI1.
old-location: properties\InitPropVariantFromGUIDAsBuffer.htm
old-project: properties
ms.assetid: 9ff3ec09-3314-4830-b970-b33f5a53d66c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: InitPropVariantFromGUIDAsBuffer, InitPropVariantFromGUIDAsBuffer function [Windows Properties], properties.InitPropVariantFromGUIDAsBuffer, propvarutil/InitPropVariantFromGUIDAsBuffer, shell.InitPropVariantFromGUIDAsBuffer, shell_InitPropVariantFromGUIDAsBuffer
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
-	HeaderDef
api_location:
-	Propvarutil.h
api_name:
-	InitPropVariantFromGUIDAsBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# InitPropVariantFromGUIDAsBuffer function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a <b>GUID</b>. The structure is initialized as VT_VECTOR | VT_UI1.


## -parameters




### -param guid [in]

Type: <b>REFGUID</b>

Reference to the source <b>GUID</b>.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_VECTOR | VT_UI1 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <b>InitPropVariantFromGUIDAsBuffer</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromGUIDAsBuffer(FMTID_DocSummaryInformation, &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_UI1.
 
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromCLSID">InitPropVariantFromCLSID</a>



<a href="https://msdn.microsoft.com/bcc343f7-741f-4cdd-bd2f-ae4786faab0e">InitPropVariantFromGUIDAsString</a>



<a href="shell.InitVariantFromGUIDAsBuffer">InitVariantFromGUIDAsBuffer</a>



<a href="shell.PropVariantToBuffer">PropVariantToBuffer</a>
 

 

