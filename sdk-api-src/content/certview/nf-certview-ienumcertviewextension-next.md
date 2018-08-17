---
UID: NF:certview.IEnumCERTVIEWEXTENSION.Next
title: IEnumCERTVIEWEXTENSION::Next
author: windows-sdk-content
description: Moves to the next extension in the extension-enumeration sequence.
old-location: security\ienumcertviewextension_next.htm
old-project: SecCrypto
ms.assetid: 658daf9d-0f61-4c93-9688-a7c74464ca89
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: IEnumCERTVIEWEXTENSION interface [Security],Next method, IEnumCERTVIEWEXTENSION object [Security],Next method, IEnumCERTVIEWEXTENSION.Next, IEnumCERTVIEWEXTENSION::Next, Next, Next method [Security], Next method [Security],IEnumCERTVIEWEXTENSION interface, Next method [Security],IEnumCERTVIEWEXTENSION object, _certsrv_ienumcertviewextension_next, certview/IEnumCERTVIEWEXTENSION::Next, security.ienumcertviewextension_next
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
 - IEnumCERTVIEWEXTENSION.Next
 - IEnumCERTVIEWEXTENSION.Next
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# IEnumCERTVIEWEXTENSION::Next


## -description


The <b>Next</b> method moves to the next extension in the extension-enumeration sequence.


## -parameters




### -param pIndex [out]

A pointer to a variable that contains the index value of the next extension being referenced. If there are no more extensions to enumerate, this variable will be set to –1. This method fails if <i>pIndex</i> is <b>NULL</b>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK and the next extension is now being referenced. If there are no more extensions, S_FALSE is returned, and the  <i>pIndex</i> parameter is set to a value of –1.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the index value of the extension that is now referenced by the extension-enumeration sequence. If there are no more extensions to enumerate, the return value is –1.




## -remarks



Upon successful completion of this method, the extension name, flags, and value can be accessed through 
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
<pre>LONG  Index;
LONG  nCount;

// determine the number of extensions
nCount = 0;
// pEnumExt is previously instantiated IEnumCERTVIEWEXTENSION object
while (S_OK == pEnumExt-&gt;Next(&amp;Index))
{
    nCount++;
}
printf("Number of extensions is %d\n", nCount);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa386203(v=VS.85).aspx">IEnumCERTVIEWEXTENSION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386208(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::GetFlags</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386211(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::GetName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa386216(v=VS.85).aspx">IEnumCERTVIEWEXTENSION::GetValue</a>
 

 

