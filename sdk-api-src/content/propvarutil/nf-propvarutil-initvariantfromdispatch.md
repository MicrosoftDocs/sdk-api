---
UID: NF:propvarutil.InitVariantFromDispatch
title: InitVariantFromDispatch function
author: windows-sdk-content
description: Initializes a VARIANT structure based on an instance of an IDispatch object.
old-location: properties\InitVariantFromDispatch.htm
old-project: properties
ms.assetid: d42c48b5-cfd9-4de8-b0aa-b108d242e2e9
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: InitVariantFromDispatch, InitVariantFromDispatch function [Windows Properties], _shell_InitVariantFromDispatch, properties.InitVariantFromDispatch, propvarutil/InitVariantFromDispatch, shell.InitVariantFromDispatch
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
-	InitVariantFromDispatch
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# InitVariantFromDispatch function


## -description


Initializes a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure based on an instance of an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> object.


## -parameters




### -param pdisp [in]

Type: <b><a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>*</b>

Pointer to the source <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a <b>VT_DISPATCH</b> variant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitVariantFromDispatch">InitVariantFromDispatch</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IDispatch *pDispatch;
// Assume variable pDispatch is initialized and valid.
VARIANT var;

HRESULT hr = InitVariantFromDispatch(pDispatch, &amp;var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_DISPATCH.
    VariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>


