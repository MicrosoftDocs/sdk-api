---
UID: NF:certview.IEnumCERTVIEWEXTENSION.Skip
title: IEnumCERTVIEWEXTENSION::Skip
author: windows-driver-content
description: Skips a specified number of extensions in the extension-enumeration sequence.
old-location: security\ienumcertviewextension_skip.htm
old-project: SecCrypto
ms.assetid: b354cf0e-2f15-42a5-8e84-4db9bc4e6a8d
ms.author: windowsdriverdev
ms.date: 5/21/2018
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
req.typenames: ENUM_CATYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certadm.dll
api_name:
-	IEnumCERTVIEWEXTENSION.Skip
-	IEnumCERTVIEWEXTENSION.Skip
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
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

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Upon successful completion of this method, call  the 
<a href="https://msdn.microsoft.com/658daf9d-0f61-4c93-9688-a7c74464ca89">IEnumCERTVIEWEXTENSION::Next</a> method to reference the current extension in the extension-enumeration sequence. The extension name, flags, and value can be accessed through 
the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/7c56708c-ae25-46f5-94f3-d58eea8d08d4">IEnumCERTVIEWEXTENSION::GetName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c175eba9-ea7c-4018-876a-2db732cb57c4">IEnumCERTVIEWEXTENSION::GetFlags</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7a81b096-36ba-416a-ad15-5bf1c4d512dd">IEnumCERTVIEWEXTENSION::GetValue</a>
</li>
</ul>
The extension-enumeration sequence maintains an internal zero-based index. The call to the  <b>Skip</b> method causes this index to increase or  decrease by the number of extensions specified in the  <i>celt</i> parameter.

If a negative value of the <i>celt</i> parameter causes the index to be less than zero, the behavior of subsequent calls to <a href="https://msdn.microsoft.com/658daf9d-0f61-4c93-9688-a7c74464ca89">IEnumCERTVIEWEXTENSION::Next</a> is undefined.

If a positive value of the <i>celt</i> parameter causes the index to exceed the last extension in the enumeration sequence, a subsequent call to the <a href="https://msdn.microsoft.com/658daf9d-0f61-4c93-9688-a7c74464ca89">IEnumCERTVIEWEXTENSION::Next</a> method will fail.


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




<a href="https://msdn.microsoft.com/d5acff51-06f8-4a6f-aa9e-97ba052b1b34">IEnumCERTVIEWEXTENSION</a>



<a href="https://msdn.microsoft.com/c175eba9-ea7c-4018-876a-2db732cb57c4">IEnumCERTVIEWEXTENSION::GetFlags</a>



<a href="https://msdn.microsoft.com/7c56708c-ae25-46f5-94f3-d58eea8d08d4">IEnumCERTVIEWEXTENSION::GetName</a>



<a href="https://msdn.microsoft.com/7a81b096-36ba-416a-ad15-5bf1c4d512dd">IEnumCERTVIEWEXTENSION::GetValue</a>



<a href="https://msdn.microsoft.com/658daf9d-0f61-4c93-9688-a7c74464ca89">IEnumCERTVIEWEXTENSION::Next</a>
 

 

