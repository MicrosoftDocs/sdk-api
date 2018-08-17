---
UID: NF:certview.IEnumCERTVIEWEXTENSION.Reset
title: IEnumCERTVIEWEXTENSION::Reset
author: windows-sdk-content
description: Moves to the beginning of the extension-enumeration sequence.
old-location: security\ienumcertviewextension_reset.htm
old-project: SecCrypto
ms.assetid: 7af29b1f-5b43-4ab7-81fa-d03e065f014f
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: IEnumCERTVIEWEXTENSION interface [Security],Reset method, IEnumCERTVIEWEXTENSION object [Security],Reset method, IEnumCERTVIEWEXTENSION.Reset, IEnumCERTVIEWEXTENSION::Reset, Reset, Reset method [Security], Reset method [Security],IEnumCERTVIEWEXTENSION interface, Reset method [Security],IEnumCERTVIEWEXTENSION object, _certsrv_ienumcertviewextension_reset, certview/IEnumCERTVIEWEXTENSION::Reset, security.ienumcertviewextension_reset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certview.h
req.include-header: Certsrv.h
req.redist: 
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
 - IEnumCERTVIEWEXTENSION.Reset
 - IEnumCERTVIEWEXTENSION.Reset
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# IEnumCERTVIEWEXTENSION::Reset


## -description


The <b>Reset</b> method moves to the beginning of the extension-enumeration sequence.


## -parameters






## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



Upon successful completion of this method, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa386220(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::Next</a> method to reference the first extension in the extension-enumeration sequence.

The extension name, flags, and value can be accessed through 
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
hr = pEnumExt-&gt;Reset();
if (S_OK != hr)
    printf("Unable to reset pEnumExt - %x\n", hr);
    // call appropriate error handler / exit routine
else
{
    // reset to beginning of extensions again
    while (S_OK == pEnumExt-&gt;Next(&amp;Index))
    {
        // Use each extension as needed.
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
 

 

