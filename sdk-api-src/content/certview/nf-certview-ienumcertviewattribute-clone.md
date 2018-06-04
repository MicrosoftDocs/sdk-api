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

# IEnumCERTVIEWATTRIBUTE::Clone


## -description


The <b>Clone</b> method creates a copy of the attribute-enumeration sequence object in its current state.


## -parameters




### -param ppenum [out]

A pointer to a pointer of <a href="https://msdn.microsoft.com/fc1eb29d-27d9-4331-b588-dc0632b3db6a">IEnumCERTVIEWATTRIBUTE</a> type. This function will fail if <i>ppenum</i> is <b>NULL</b>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a cloned attribute-enumeration sequence object.




## -remarks



The attribute-enumeration sequence object is obtained by a call to 
the <a href="https://msdn.microsoft.com/53a70f66-3805-429e-8ef6-01b00b666b72">IEnumCERTVIEWROW::EnumCertViewAttribute</a> method.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// pEnumAttr is previously instantiated IEnumCERTVIEWATTRIBUTE object
IEnumCERTVIEWATTRIBUTE * pEnumAttr2 = NULL;
HRESULT    hr;
hr = pEnumAttr-&gt;Clone(&amp;pEnumAttr2);
if (S_OK != hr)
    printf("Unable to clone IEnumCERTVIEWATTRIBUTE\n");
else
{
    // use cloned object as needed
    // ...
}
// done using cloned object, free memory
if (NULL != pEnumAttr2)
    pEnumAttr2-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fc1eb29d-27d9-4331-b588-dc0632b3db6a">IEnumCERTVIEWATTRIBUTE</a>
 

 

