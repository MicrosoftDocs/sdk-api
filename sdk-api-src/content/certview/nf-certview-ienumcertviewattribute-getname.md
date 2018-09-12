---
UID: NF:certview.IEnumCERTVIEWATTRIBUTE.GetName
title: IEnumCERTVIEWATTRIBUTE::GetName
author: windows-sdk-content
description: Retrieves the name of the current attribute in the attribute-enumeration sequence.
old-location: security\ienumcertviewattribute_getname.htm
tech.root: seccrypto
ms.assetid: c2409bf1-0571-479e-8499-010d52cfb776
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetName, GetName method [Security], GetName method [Security],IEnumCERTVIEWATTRIBUTE interface, IEnumCERTVIEWATTRIBUTE interface [Security],GetName method, IEnumCERTVIEWATTRIBUTE.GetName, IEnumCERTVIEWATTRIBUTE::GetName, _certsrv_ienumcertviewattribute_getname, certview/IEnumCERTVIEWATTRIBUTE::GetName, security.ienumcertviewattribute_getname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certview.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IEnumCERTVIEWATTRIBUTE.GetName
 - IEnumCERTVIEWATTRIBUTE.GetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWATTRIBUTE::GetName


## -description


The <b>GetName</b> method retrieves the name of the current attribute in the attribute-enumeration sequence.


## -parameters




### -param pstrOut [out]

A pointer to a variable of <b>BSTR</b> type that contains the name of the attribute.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK and the <i>pstrOut</i> parameter contains the name of the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a>.

To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrOut</i>. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>String</b> that contains the name of the attribute.




## -remarks



This method is used to retrieve the name of the attribute currently referenced by the 
attribute-enumeration sequence.

If the attribute-enumeration sequence is not referencing a valid attribute, <b>GetName</b> will fail. Use one of the following methods to navigate through the enumeration:

<ul>
<li>
<a href="https://msdn.microsoft.com/1f5b8ee0-2820-481b-8836-b2926aec0933">IEnumCERTVIEWATTRIBUTE::Reset</a>: Moves to the beginning of the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/2903ccda-e06d-4690-accf-79bc73d8569f">IEnumCERTVIEWATTRIBUTE::Next</a>: Moves to the next attribute in the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/546e7ad7-73f2-4f6e-8d02-a9ca5401ecce">IEnumCERTVIEWATTRIBUTE::Skip</a>: Skips a specified number of attributes.</li>
</ul>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BSTR    bstrAttribName = NULL;

// pEnumAttr is previously instantiated IEnumCERTVIEWATTRIBUTE object
hr = pEnumAttr-&gt;GetName(&amp;bstrAttribName);
if (S_OK != hr)
    printf("Failed call to GetName - %x\n", hr);
else
    printf("Attribute name is %ws\n", bstrAttribName );

// free memory when done
if (NULL != bstrAttribName)
    SysFreeString(bstrAttribName);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fc1eb29d-27d9-4331-b588-dc0632b3db6a">IEnumCERTVIEWATTRIBUTE</a>



<a href="https://msdn.microsoft.com/a03a6da4-d286-487e-a292-8a02626325a8">IEnumCERTVIEWATTRIBUTE::GetValue</a>



<a href="https://msdn.microsoft.com/2903ccda-e06d-4690-accf-79bc73d8569f">IEnumCERTVIEWATTRIBUTE::Next</a>



<a href="https://msdn.microsoft.com/1f5b8ee0-2820-481b-8836-b2926aec0933">IEnumCERTVIEWATTRIBUTE::Reset</a>



<a href="https://msdn.microsoft.com/546e7ad7-73f2-4f6e-8d02-a9ca5401ecce">IEnumCERTVIEWATTRIBUTE::Skip</a>
 

 

