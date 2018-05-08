---
UID: NF:propvarutil.InitVariantFromGUIDAsBuffer
title: InitVariantFromGUIDAsBuffer function
author: windows-driver-content
description: Initializes a VARIANT structure based on a GUID. The structure is initialized as VT_ARRAY | VT_UI1.
old-location: properties\InitVariantFromGUIDAsBuffer.htm
old-project: properties
ms.assetid: c46c1263-527a-4a64-b4c9-4c4779b271c7
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: InitVariantFromGUIDAsBuffer, InitVariantFromGUIDAsBuffer function [Windows Properties], properties.InitVariantFromGUIDAsBuffer, propvarutil/InitVariantFromGUIDAsBuffer, shell.InitVariantFromGUIDAsBuffer, shell_InitVariantFromGUIDAsBuffer
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
-	HeaderDef
api_location:
-	Propvarutil.h
api_name:
-	InitVariantFromGUIDAsBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# InitVariantFromGUIDAsBuffer function


## -description


Initializes a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure based on a <b>GUID</b>. The structure is initialized as VT_ARRAY | VT_UI1.


## -parameters




### -param guid [in]

Type: <b>REFGUID</b>

Reference to the source <b>GUID</b>.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitVariantFromGUIDAsBuffer">InitVariantFromGUIDAsBuffer</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VARIANT var;

HRESULT hr = InitVariantFromGUIDAsBuffer(FMTID_DocSummaryInformation, &amp;var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_ARRAY | VT_UI1.
    VariantClear(&amp;var);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromCLSID">InitPropVariantFromCLSID</a>



<a href="https://msdn.microsoft.com/2a78257a-a8ce-45e8-aea2-dfa9f380528a">InitVariantFromGUIDAsString</a>



<a href="shell.VariantToBuffer">VariantToBuffer</a>
 

 

