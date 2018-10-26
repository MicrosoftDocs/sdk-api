---
UID: NF:certview.IEnumCERTVIEWATTRIBUTE.Skip
title: IEnumCERTVIEWATTRIBUTE::Skip
author: windows-sdk-content
description: Skips a specified number of attributes in the attribute-enumeration sequence.
old-location: security\ienumcertviewattribute_skip.htm
tech.root: seccrypto
ms.assetid: 546e7ad7-73f2-4f6e-8d02-a9ca5401ecce
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IEnumCERTVIEWATTRIBUTE interface [Security],Skip method, IEnumCERTVIEWATTRIBUTE object [Security],Skip method, IEnumCERTVIEWATTRIBUTE.Skip, IEnumCERTVIEWATTRIBUTE::Skip, Skip, Skip method [Security], Skip method [Security],IEnumCERTVIEWATTRIBUTE interface, Skip method [Security],IEnumCERTVIEWATTRIBUTE object, _certsrv_ienumcertviewattribute_skip, certview/IEnumCERTVIEWATTRIBUTE::Skip, security.ienumcertviewattribute_skip
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
 - IEnumCERTVIEWATTRIBUTE.Skip
 - IEnumCERTVIEWATTRIBUTE.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWATTRIBUTE::Skip


## -description


The <b>Skip</b> method skips a specified number of attributes in the attribute-enumeration sequence.


## -parameters




### -param celt [in]

The number of attributes to skip. A positive value for the <i>celt</i> parameter  causes the attribute-enumeration sequence to skip forward in the sequence. A negative value for the <i>celt</i> parameter causes the attribute-enumeration sequence to skip backward in the sequence.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

A return value of E_INVALIDARG indicates that a negative value for the <i>celt</i> parameter caused the attribute-enumeration sequence index to become less than zero.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Upon successful completion of this method, call the 
<a href="https://msdn.microsoft.com/2903ccda-e06d-4690-accf-79bc73d8569f">IEnumCERTVIEWATTRIBUTE::Next</a> method to reference the current attribute in the attribute-enumeration sequence.  The attribute name and value can be accessed through the 
following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/c2409bf1-0571-479e-8499-010d52cfb776">IEnumCERTVIEWATTRIBUTE::GetName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a03a6da4-d286-487e-a292-8a02626325a8">IEnumCERTVIEWATTRIBUTE::GetValue</a>
</li>
</ul>
The attribute-enumeration sequence maintains an internal  zero-based index. The call to the <a href="https://msdn.microsoft.com/fc1eb29d-27d9-4331-b588-dc0632b3db6a">Skip</a> method causes this index to increase or decrease by the number of attributes specified in the  <i>celt</i> parameter.

If a negative value of the <i>celt</i> parameter causes the index to be less than zero, the behavior of subsequent calls to <a href="https://msdn.microsoft.com/2903ccda-e06d-4690-accf-79bc73d8569f">IEnumCERTVIEWATTRIBUTE::Next</a> is undefined.

If a positive value of the <i>celt</i> parameter causes the  index to exceed the last attribute in the enumeration sequence, a subsequent call to the <a href="https://msdn.microsoft.com/2903ccda-e06d-4690-accf-79bc73d8569f">IEnumCERTVIEWATTRIBUTE::Next</a> method will fail.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT  hr;
LONG     Index;

// pEnumAttr is previously instantiated IEnumCERTVIEWATTRIBUTE object
// skip the next 5 attributes
hr = pEnumAttr-&gt;Skip(5);
if (S_OK == hr)
{
    // get the next attribute
    hr = pEnumAttr-&gt;Next(&amp;Index);
    if (S_OK == hr)
    {
        // Use this attribute as needed.
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fc1eb29d-27d9-4331-b588-dc0632b3db6a">IEnumCERTVIEWATTRIBUTE</a>



<a href="https://msdn.microsoft.com/1f5b8ee0-2820-481b-8836-b2926aec0933">IEnumCERTVIEWATTRIBUTE::Reset</a>



<a href="https://msdn.microsoft.com/2903ccda-e06d-4690-accf-79bc73d8569f">IEnumCERTVIEWATTRIBUTE:Next</a>
 

 

