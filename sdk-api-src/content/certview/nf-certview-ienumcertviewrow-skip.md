---
UID: NF:certview.IEnumCERTVIEWROW.Skip
title: IEnumCERTVIEWROW::Skip
author: windows-sdk-content
description: Skips a specified number of rows in the row enumeration sequence.
old-location: security\ienumcertviewrow_skip.htm
tech.root: seccrypto
ms.assetid: 9115262e-00bb-4446-906d-7a57fd5781d1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumCERTVIEWROW interface [Security],Skip method, IEnumCERTVIEWROW object [Security],Skip method, IEnumCERTVIEWROW.Skip, IEnumCERTVIEWROW::Skip, Skip, Skip method [Security], Skip method [Security],IEnumCERTVIEWROW interface, Skip method [Security],IEnumCERTVIEWROW object, _certsrv_ienumcertviewrow_skip, certview/IEnumCERTVIEWROW::Skip, security.ienumcertviewrow_skip
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
 - IEnumCERTVIEWROW.Skip
 - IEnumCERTVIEWROW.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWROW::Skip


## -description


The <b>Skip</b> method skips a specified number of rows in the 
row enumeration sequence.


## -parameters




### -param celt [in]

The number of rows to skip. A positive value for the <i>celt</i> parameter causes the row-enumeration sequence to skip forward in the enumeration sequence. A negative value for the <i>celt</i> parameter causes the row enumeration sequence to skip backward in the enumeration sequence.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

A return value of E_INVALIDARG indicates that the <i>celt</i> parameter was set to a negative number which caused the row-enumeration sequence  index to become less than zero.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Upon successful completion of this method, call  the 
<b>IEnumCERTVIEWROW::Skip</b> method to reference the current row in the row-enumeration sequence. After this second call is made, the 
columns, attributes, and extensions associated with the certificate in the row can be enumerated using the methods of the following interfaces:

<ul>
<li>
<a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fc1eb29d-27d9-4331-b588-dc0632b3db6a">IEnumCERTVIEWATTRIBUTE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d5acff51-06f8-4a6f-aa9e-97ba052b1b34">IEnumCERTVIEWEXTENSION</a>
</li>
</ul>
The row-enumeration sequence maintains an internal  zero-based index. The call to the <b>Skip</b> method causes this index to increase or decrease based on the setting of the <i>celt</i> parameter.

If a negative value of the <i>celt</i> parameter causes the index to be less than zero, the behavior of subsequent calls to <a href="https://msdn.microsoft.com/6e471ee9-4b69-468c-a724-e43bd93419d9">Next</a> is undefined.

If a positive value of the <i>celt</i> parameter causes the index to exceed the last row in the enumeration sequence, a subsequent call to the <a href="https://msdn.microsoft.com/6e471ee9-4b69-468c-a724-e43bd93419d9">Next</a> method will fail.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// pEnumRow is previously instantiated pointer to IEnumCERTVIEWROW.
HRESULT  hr;
LONG     Index;
// Reposition the row enumerator to the beginning of the rows.
hr = pEnumRow-&gt;Reset();
if (FAILED(hr))
{
    printf("Unable to reset pEnumRow\n");
    goto error;
}
// Skip some rows.
hr = pEnumRow-&gt;Skip(5);
if (FAILED(hr))
{
    printf("Unable to skip rows\n");
    goto error;
}

// Get the next row.
hr = pEnumRow-&gt;Next(&amp;Index);
if (S_OK == hr)
{
    // Use this row as needed.
}

error:

if (NULL != pEnumRow)
    pEnumRow-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fc1eb29d-27d9-4331-b588-dc0632b3db6a">IEnumCERTVIEWATTRIBUTE</a>



<a href="https://msdn.microsoft.com/6e6547f9-44b2-4050-be90-ac8ede892adc">IEnumCERTVIEWCOLUMN</a>



<a href="https://msdn.microsoft.com/d5acff51-06f8-4a6f-aa9e-97ba052b1b34">IEnumCERTVIEWEXTENSION</a>



<a href="https://msdn.microsoft.com/c9529f7a-9d97-4315-af96-f7b687af3c2e">IEnumCERTVIEWROW</a>



<a href="https://msdn.microsoft.com/6e471ee9-4b69-468c-a724-e43bd93419d9">IEnumCERTVIEWROW::Next</a>



<a href="https://msdn.microsoft.com/76bee5db-0443-4673-a59c-0198587736dc">IEnumCERTVIEWROW::Reset</a>
 

 

