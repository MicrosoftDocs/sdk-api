---
UID: NF:certview.IEnumCERTVIEWATTRIBUTE.GetValue
title: IEnumCERTVIEWATTRIBUTE::GetValue
author: windows-sdk-content
description: Retrieves the value of the current attribute in the attribute-enumeration sequence.
old-location: security\ienumcertviewattribute_getvalue.htm
old-project: SecCrypto
ms.assetid: a03a6da4-d286-487e-a292-8a02626325a8
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: GetValue, GetValue method [Security], GetValue method [Security],IEnumCERTVIEWATTRIBUTE interface, IEnumCERTVIEWATTRIBUTE interface [Security],GetValue method, IEnumCERTVIEWATTRIBUTE.GetValue, IEnumCERTVIEWATTRIBUTE::GetValue, _certsrv_ienumcertviewattribute_getvalue, certview/IEnumCERTVIEWATTRIBUTE::GetValue, security.ienumcertviewattribute_getvalue
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ENUM_CATYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certadm.dll
api_name:
-	IEnumCERTVIEWATTRIBUTE.GetValue
-	IEnumCERTVIEWATTRIBUTE.GetValue
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# IEnumCERTVIEWATTRIBUTE::GetValue


## -description


The <b>GetValue</b> method retrieves the value of the current attribute in the attribute-enumeration sequence.


## -parameters




### -param pstrOut [out]

A pointer to a <b>BSTR</b> type that contains the value of the attribute.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK and the <i>pstrOut</i> is set to the value of the current attribute.

To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrOut</i>. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>String</b> that represents the value of the current attribute.




## -remarks



This method is used to retrieve the data in the attribute currently referenced by the 
attribute-enumeration sequence.

If the attribute-enumeration sequence is not referencing a valid attribute, <b>GetValue</b> will fail. Use 
one of the following methods to navigate through the enumeration:

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
<pre>BSTR    bstrAttribValue = NULL;

// pEnumAttr is previously instantiated IEnumCERTVIEWATTRIBUTE object
hr = pEnumAttr-&gt;GetValue(&amp;bstrAttribValue);
if (S_OK != hr)
    printf("Failed call to GetValue - %x\n", hr);
else
    printf("Attribute value is %ws\n",bstrAttribValue);

// free memory when done
if (NULL != bstrAttribValue)
    SysFreeString(bstrAttribValue);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fc1eb29d-27d9-4331-b588-dc0632b3db6a">IEnumCERTVIEWATTRIBUTE</a>



<a href="https://msdn.microsoft.com/c2409bf1-0571-479e-8499-010d52cfb776">IEnumCERTVIEWATTRIBUTE::GetName</a>



<a href="https://msdn.microsoft.com/2903ccda-e06d-4690-accf-79bc73d8569f">IEnumCERTVIEWATTRIBUTE::Next</a>



<a href="https://msdn.microsoft.com/1f5b8ee0-2820-481b-8836-b2926aec0933">IEnumCERTVIEWATTRIBUTE::Reset</a>



<a href="https://msdn.microsoft.com/546e7ad7-73f2-4f6e-8d02-a9ca5401ecce">IEnumCERTVIEWATTRIBUTE::Skip</a>
 

 

