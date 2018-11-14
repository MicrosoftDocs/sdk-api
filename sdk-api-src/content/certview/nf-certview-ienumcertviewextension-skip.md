---
UID: NF:certview.IEnumCERTVIEWEXTENSION.Skip
title: IEnumCERTVIEWEXTENSION::Skip
author: windows-sdk-content
description: Skips a specified number of extensions in the extension-enumeration sequence.
old-location: security\ienumcertviewextension_skip.htm
tech.root: seccrypto
ms.assetid: b354cf0e-2f15-42a5-8e84-4db9bc4e6a8d
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IEnumCERTVIEWEXTENSION interface [Security],Skip method, IEnumCERTVIEWEXTENSION object [Security],Skip method, IEnumCERTVIEWEXTENSION.Skip, IEnumCERTVIEWEXTENSION::Skip, Skip, Skip method [Security], Skip method [Security],IEnumCERTVIEWEXTENSION interface, Skip method [Security],IEnumCERTVIEWEXTENSION object, _certsrv_ienumcertviewextension_skip, certview/IEnumCERTVIEWEXTENSION::Skip, security.ienumcertviewextension_skip
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
 - IEnumCERTVIEWEXTENSION.Skip
 - IEnumCERTVIEWEXTENSION.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certview.h
: 
- IEnumCERTVIEWEXTENSION.Skip
: 
---

# IEnumCERTVIEWEXTENSION::Skip


## -description


The <b>Skip</b> method skips a specified number of extensions in the extension-enumeration sequence.


## -parameters




### -param celt [in]

The number of extensions to skip. A positive value for the <i>celt</i> parameter causes the extension-enumeration sequence to skip forward in the  sequence. A negative value for the <i>celt</i> parameter causes the extension-enumeration sequence  to skip backward in the  sequence.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

A return value of E_INVALIDARG indicates that a negative value for the <i>celt</i> parameter caused the extension-enumeration sequence  index to become less than zero.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



Upon successful completion of this method, call  the 
<a href="https://msdn.microsoft.com/en-us/library/Aa386220(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::Next</a> method to reference the current extension in the extension-enumeration sequence. The extension name, flags, and value can be accessed through 
the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386211(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::GetName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386208(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::GetFlags</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa386216(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::GetValue</a>
</li>
</ul>
The extension-enumeration sequence maintains an internal zero-based index. The call to the  <b>Skip</b> method causes this index to increase or  decrease by the number of extensions specified in the  <i>celt</i> parameter.

If a negative value of the <i>celt</i> parameter causes the index to be less than zero, the behavior of subsequent calls to <a href="https://msdn.microsoft.com/en-us/library/Aa386220(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::Next</a> is undefined.

If a positive value of the <i>celt</i> parameter causes the index to exceed the last extension in the enumeration sequence, a subsequent call to the <a href="https://msdn.microsoft.com/en-us/library/Aa386220(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::Next</a> method will fail.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT  hr;
LONG     Index;

// pEnumExt is previously instantiated IEnumCERTVIEWEXTENSION object
// skip the next 5 extensions
hr = pEnumExt-&gt;Skip(5);
if (S_OK == hr)
{
    // get the next extension
    hr = pEnumExt-&gt;Next(&amp;Index);
    if (S_OK == hr)
    {
        // Use this extension as needed.
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa386203(v=VS.85).aspx">IEnumCERTVIEWEXTENSION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386208(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::GetFlags</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386211(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::GetName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386216(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::GetValue</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386220(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::Next</a>
 

 

