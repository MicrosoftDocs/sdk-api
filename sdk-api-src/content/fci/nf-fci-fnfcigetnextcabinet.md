---
UID: NF:fci.FNFCIGETNEXTCABINET
title: FNFCIGETNEXTCABINET macro
author: windows-sdk-content
description: The FNFCIGETNEXTCABINET macro provides the declaration for the application-defined callback function to request information for the next cabinet.
old-location: winprog\fnfcigetnextcabinet.htm
old-project: DevNotes
ms.assetid: d56fb63e-91bf-4991-a954-176211697a2e
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: FNFCIGETNEXTCABINET, FNFCIGETNEXTCABINET macro [Windows API], fci/FNFCIGETNEXTCABINET, winprog.fnfcigetnextcabinet
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: fci.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: FAX_ROUTE_CALLBACKROUTINES, *PFAX_ROUTE_CALLBACKROUTINES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fci.h
api_name:
 - FNFCIGETNEXTCABINET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FNFCIGETNEXTCABINET macro


## -description


The <b>FNFCIGETNEXTCABINET</b> macro provides the declaration for the application-defined callback function to request information for the next cabinet.


## -parameters




### -param fn

TBD






#### - cbPrevCab

Size, in bytes, of the previous cabinet.


#### - pccab

Pointer to a <a href="https://msdn.microsoft.com/e25cb72b-4c96-40e9-9fd5-2920e4a01d3a">CCAB</a> structure to provide the parameters for the creation of a new cabinet.


#### - pv

Pointer to an application-defined value.


## -remarks



The <a href="https://msdn.microsoft.com/e25cb72b-4c96-40e9-9fd5-2920e4a01d3a">CCAB</a> structure referenced by this function is relevant to the most recently completed cabinet. However, with each successful operation the  <i>iCab</i> field contained within this structure will have incremented by 1. Additionally, the next cabinet will be created using the fields in this structure.  The szCab, in particular, should be modified as necessary. In particular, the <i>szCab</i> field, which specifies the cabinet name, should be changed for each cabinet.

When creating multiple cabinets, typically the <i>iCab</i> field is used to create the name.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNFCIGETNEXTCABINET(fnGetNextCabinet)
{
    HRESULT hr;

    UNREFERENCED_PARAMETER(pv);
    UNREFERENCED_PARAMETER(cbPrevCab);
    
    hr = StringCchPrintfA(pccab-&gt;szCab,
                          ARRAYSIZE(pccab-&gt;szCab),
                          "FCISample%02d.cab",
                          pccab-&gt;iCab);
        
    return ( SUCCEEDED(hr) );
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a>
 

 

