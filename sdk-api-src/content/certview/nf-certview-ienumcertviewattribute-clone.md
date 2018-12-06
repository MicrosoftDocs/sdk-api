---
UID: NF:certview.IEnumCERTVIEWATTRIBUTE.Clone
title: IEnumCERTVIEWATTRIBUTE::Clone
author: windows-sdk-content
description: Creates a copy of the attribute-enumeration sequence object in its current state.
old-location: security\ienumcertviewattribute_clone.htm
tech.root: seccrypto
ms.assetid: 6144514a-cd64-42ce-a856-ff942b129e5a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [Security], Clone method [Security],IEnumCERTVIEWATTRIBUTE interface, IEnumCERTVIEWATTRIBUTE interface [Security],Clone method, IEnumCERTVIEWATTRIBUTE.Clone, IEnumCERTVIEWATTRIBUTE::Clone, _certsrv_ienumcertviewattribute_clone, certview/IEnumCERTVIEWATTRIBUTE::Clone, security.ienumcertviewattribute_clone
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
 - IEnumCERTVIEWATTRIBUTE.Clone
 - IEnumCERTVIEWATTRIBUTE.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCERTVIEWATTRIBUTE::Clone


## -description


The <b>Clone</b> method creates a copy of the attribute-enumeration sequence object in its current state.


## -parameters




### -param ppenum [out]

A pointer to a pointer of <a href="https://msdn.microsoft.com/fc1eb29d-27d9-4331-b588-dc0632b3db6a">IEnumCERTVIEWATTRIBUTE</a> type. This function will fail if <i>ppenum</i> is <b>NULL</b>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a cloned attribute-enumeration sequence object.




## -remarks



The attribute-enumeration sequence object is obtained by a call to 
the <a href="https://msdn.microsoft.com/53a70f66-3805-429e-8ef6-01b00b666b72">IEnumCERTVIEWROW::EnumCertViewAttribute</a> method.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// pEnumAttr is previously instantiated IEnumCERTVIEWATTRIBUTE object
IEnumCERTVIEWATTRIBUTE * pEnumAttr2 = NULL;
HRESULT    hr;
hr = pEnumAttr-&gt;Clone(&amp;pEnumAttr2);
if (S_OK != hr)
    printf("Unable to clone IEnumCERTVIEWATTRIBUTE\n");
else
{
    // use cloned object as needed
    // ...
}
// done using cloned object, free memory
if (NULL != pEnumAttr2)
    pEnumAttr2-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fc1eb29d-27d9-4331-b588-dc0632b3db6a">IEnumCERTVIEWATTRIBUTE</a>
 

 

