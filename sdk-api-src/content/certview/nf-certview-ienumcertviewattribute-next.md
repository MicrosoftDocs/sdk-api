---
UID: NF:certview.IEnumCERTVIEWATTRIBUTE.Next
title: IEnumCERTVIEWATTRIBUTE::Next
author: windows-sdk-content
description: Moves to the next attribute in the attribute-enumeration sequence.
old-location: security\ienumcertviewattribute_next.htm
tech.root: seccrypto
ms.assetid: 2903ccda-e06d-4690-accf-79bc73d8569f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IEnumCERTVIEWATTRIBUTE interface [Security],Next method, IEnumCERTVIEWATTRIBUTE.Next, IEnumCERTVIEWATTRIBUTE::Next, Next, Next method [Security], Next method [Security],IEnumCERTVIEWATTRIBUTE interface, _certsrv_ienumcertviewattribute_next, certview/IEnumCERTVIEWATTRIBUTE::Next, security.ienumcertviewattribute_next
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
 - IEnumCERTVIEWATTRIBUTE.Next
 - IEnumCERTVIEWATTRIBUTE.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWATTRIBUTE::Next


## -description


The <b>Next</b> method moves to the next  attribute in the attribute-enumeration sequence.


## -parameters




### -param pIndex [out]

A pointer to a variable that contains the index value of the next <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">attribute</a> being referenced. If there are no more attributes to enumerate, this variable is set to –1. This method fails if <i>pIndex</i> is <b>NULL</b>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK and  the next attribute is now being referenced by the attribute-enumeration sequence.  If there are no more attributes, the method returns S_FALSE, and <i>pIndex</i> is set to a value of –1.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the index value of the attribute that is now referenced by the attribute-enumeration sequence. If there are no more attributes to enumerate, the return value is –1.




## -remarks



Upon successful completion of this method, the attribute name and value can be accessed through the 
following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386164(v=VS.85).aspx">IEnumCERTVIEWATTRIBUTE::GetName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386166(v=VS.85).aspx">IEnumCERTVIEWATTRIBUTE::GetValue</a>
</li>
</ul>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>LONG       Index;
HRESULT    hr;
BSTR       bstrAttribName = NULL;

// pEnumAttr is previously instantiated IEnumCERTVIEWATTRIBUTE object
while (S_OK == pEnumAttr-&gt;Next(&amp;Index))
{
    // retrieve the attribute name
    hr = pEnumAttr-&gt;GetName(&amp;bstrAttribName);
    if (FAILED(hr))
        printf("Failed GetName -  %x\n", hr );
    else
        printf("Attribute name: %ws\n", bstrAttribName);
}

// Free resources.
if (NULL != bstrAttribName)
    SysFreeString(bstrAttribName);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa386157(v=VS.85).aspx">IEnumCERTVIEWATTRIBUTE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386164(v=VS.85).aspx">IEnumCERTVIEWATTRIBUTE::GetName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386166(v=VS.85).aspx">IEnumCERTVIEWATTRIBUTE::GetValue</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386170(v=VS.85).aspx">IEnumCERTVIEWATTRIBUTE::Reset</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386172(v=VS.85).aspx">IEnumCERTVIEWATTRIBUTE::Skip</a>
 

 

