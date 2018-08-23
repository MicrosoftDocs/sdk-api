---
UID: NF:certif.ICertServerExit.EnumerateAttributesSetup
title: ICertServerExit::EnumerateAttributesSetup
author: windows-sdk-content
description: Initializes the internal enumeration pointer to the first request attribute associated with the current context.
old-location: security\icertserverexit_enumerateattributessetup.htm
old-project: SecCrypto
ms.assetid: c81b9c4d-483e-48b8-a270-f570e148d371
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CCertServerExit object [Security],EnumerateAttributesSetup method, EnumerateAttributesSetup, EnumerateAttributesSetup method [Security], EnumerateAttributesSetup method [Security],CCertServerExit object, EnumerateAttributesSetup method [Security],ICertServerExit interface, ICertServerExit interface [Security],EnumerateAttributesSetup method, ICertServerExit.EnumerateAttributesSetup, ICertServerExit::EnumerateAttributesSetup, _certsrv_icertserverexit_enumerateattributessetup, certif/ICertServerExit::EnumerateAttributesSetup, security.icertserverexit_enumerateattributessetup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certif.h
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
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertServerExit.EnumerateAttributesSetup
 - CCertServerExit.EnumerateAttributesSetup
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
---

# ICertServerExit::EnumerateAttributesSetup


## -description


The <b>EnumerateAttributesSetup</b> method initializes the internal enumeration pointer to the first request attribute associated with the current context.


## -parameters




### -param Flags [in]

This parameter is reserved and must be set to zero.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



You must call 
<a href="https://msdn.microsoft.com/en-us/library/Aa385079(v=VS.85).aspx">ICertServerExit::SetContext</a> prior to using this method.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Set up the enumeration.
hr = pCertServerExit-&gt;EnumerateAttributesSetup(0);
if (FAILED(hr))
{
    printf("Failed EnumerateAttributesSetup [%x]\n", hr);
    goto error;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa385055(v=VS.85).aspx">ICertServerExit</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385056(v=VS.85).aspx">ICertServerExit::EnumerateAttributes</a>
 

 

