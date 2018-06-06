---
UID: NF:certview.IEnumCERTVIEWROW.EnumCertViewExtension
title: IEnumCERTVIEWROW::EnumCertViewExtension
author: windows-sdk-content
description: Obtains an instance of an extension-enumeration sequence for the current row of the row-enumeration sequence.
old-location: security\ienumcertviewrow_enumcertviewextension.htm
old-project: SecCrypto
ms.assetid: 41028000-fa87-4ad0-93fc-314c5d3870f9
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: EnumCertViewExtension, EnumCertViewExtension method [Security], EnumCertViewExtension method [Security],IEnumCERTVIEWROW interface, IEnumCERTVIEWROW interface [Security],EnumCertViewExtension method, IEnumCERTVIEWROW.EnumCertViewExtension, IEnumCERTVIEWROW::EnumCertViewExtension, _certsrv_ienumcertviewrow_enumcertviewextension, certview/IEnumCERTVIEWROW::EnumCertViewExtension, security.ienumcertviewrow_enumcertviewextension
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IEnumCERTVIEWROW.EnumCertViewExtension
 - IEnumCERTVIEWROW.EnumCertViewExtension
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# IEnumCERTVIEWROW::EnumCertViewExtension


## -description


The <b>EnumCertViewExtension</b> method obtains an instance of an extension-enumeration sequence for the current row of the row-enumeration sequence.


## -parameters




### -param Flags [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td>
A <b>LONG</b> value. Must be zero.

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>
A <b>Long</b> value. Must be zero.

</td>
</tr>
</table>

### -param ppenum [out, retval]

A pointer to a pointer of <a href="https://msdn.microsoft.com/d5acff51-06f8-4a6f-aa9e-97ba052b1b34">IEnumCERTVIEWEXTENSION</a> type.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is an extension-enumeration sequence object.




## -remarks



The 
extension-enumeration sequence obtained by this call can be used to enumerate the extensions associated with the certificate in the current row. This enumeration can be accessed through the methods of the <a href="https://msdn.microsoft.com/d5acff51-06f8-4a6f-aa9e-97ba052b1b34">IEnumCERTVIEWEXTENSION</a> interface.

To reference a different row, call one of the following methods to navigate through the row-enumeration sequence:

<ul>
<li>
<a href="https://msdn.microsoft.com/76bee5db-0443-4673-a59c-0198587736dc">IEnumCERTVIEWROW::Reset</a>: Moves to the beginning of the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/6e471ee9-4b69-468c-a724-e43bd93419d9">IEnumCERTVIEWROW::Next</a>: Moves to the next row in the enumeration sequence.</li>
<li>
<a href="https://msdn.microsoft.com/9115262e-00bb-4446-906d-7a57fd5781d1">IEnumCERTVIEWROW::Skip</a>: Skips a specified number of rows.</li>
</ul>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// pEnumRow is previously instantiated pointer to IEnumCERTVIEWROW.
LONG       Index;
HRESULT    hr;
IEnumCERTVIEWEXTENSION * pEnumExt = NULL;
// Obtain enumerator for extensions.
hr = pEnumRow-&gt;EnumCertViewExtension(0, &amp;pEnumExt);
if (FAILED(hr))
{
    printf("Failed EnumCertViewExtension - %x\n", hr);
    goto error;
}
// Enumerate each extension.
while (S_OK == pEnumExt-&gt;Next(&amp;Index))
{
    // Use this extension as needed.
}
error:

// Free resources.
if (NULL != pEnumExt)
    pEnumExt-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d5acff51-06f8-4a6f-aa9e-97ba052b1b34">IEnumCERTVIEWEXTENSION</a>



<a href="https://msdn.microsoft.com/c9529f7a-9d97-4315-af96-f7b687af3c2e">IEnumCERTVIEWROW</a>



<a href="https://msdn.microsoft.com/6e471ee9-4b69-468c-a724-e43bd93419d9">IEnumCERTVIEWROW::Next</a>



<a href="https://msdn.microsoft.com/76bee5db-0443-4673-a59c-0198587736dc">IEnumCERTVIEWROW::Reset</a>



<a href="https://msdn.microsoft.com/9115262e-00bb-4446-906d-7a57fd5781d1">IEnumCERTVIEWROW::Skip</a>
 

 

