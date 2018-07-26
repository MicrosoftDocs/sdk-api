---
UID: NF:propvarutil.InitPropVariantFromGUIDAsString
title: InitPropVariantFromGUIDAsString function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a GUID. The structure is initialized as VT_LPWSTR.
old-location: properties\InitPropVariantFromGUIDAsString.htm
old-project: properties
ms.assetid: bcc343f7-741f-4cdd-bd2f-ae4786faab0e
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: InitPropVariantFromGUIDAsString, InitPropVariantFromGUIDAsString function [Windows Properties], properties.InitPropVariantFromGUIDAsString, propvarutil/InitPropVariantFromGUIDAsString, shell.InitPropVariantFromGUIDAsString, shell_InitPropVariantFromGUIDAsString
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
 - InitPropVariantFromGUIDAsString
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# InitPropVariantFromGUIDAsString function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a <b>GUID</b>. The structure is initialized as VT_LPWSTR.


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



Creates a VT_LPWSTR <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>, which formats the GUID in a form similar to <code>{c200e360-38c5-11ce-ae62-08002b2b79ef}</code>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <b>InitPropVariantFromGUIDAsString</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromGUIDAsString(FMTID_DocSummaryInformation, &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_LPWSTR.
 
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/Bb762290(v=VS.85).aspx">InitPropVariantFromCLSID</a>



<a href="https://msdn.microsoft.com/9ff3ec09-3314-4830-b970-b33f5a53d66c">InitPropVariantFromGUIDAsBuffer</a>



<a href="https://msdn.microsoft.com/2a78257a-a8ce-45e8-aea2-dfa9f380528a">InitVariantFromGUIDAsString</a>



<a href="https://msdn.microsoft.com/library/Bb776559(v=VS.85).aspx">PropVariantToString</a>
 

 

