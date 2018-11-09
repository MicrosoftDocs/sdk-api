---
UID: NF:certif.ICertServerPolicy.EnumerateAttributesSetup
title: ICertServerPolicy::EnumerateAttributesSetup
author: windows-sdk-content
description: Initializes the internal enumeration pointer to the first request attribute associated with the current context.
old-location: security\icertserverpolicy_enumerateattributessetup.htm
tech.root: seccrypto
ms.assetid: 14b81b88-36db-4b01-96e6-eafed22ae02e
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CCertServerPolicy object [Security],EnumerateAttributesSetup method, EnumerateAttributesSetup, EnumerateAttributesSetup method [Security], EnumerateAttributesSetup method [Security],CCertServerPolicy object, EnumerateAttributesSetup method [Security],ICertServerPolicy interface, ICertServerPolicy interface [Security],EnumerateAttributesSetup method, ICertServerPolicy.EnumerateAttributesSetup, ICertServerPolicy::EnumerateAttributesSetup, _certsrv_icertserverpolicy_enumerateattributessetup, certif/ICertServerPolicy::EnumerateAttributesSetup, security.icertserverpolicy_enumerateattributessetup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certif.h
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
req.dll: Certcli.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertServerPolicy.EnumerateAttributesSetup
 - CCertServerPolicy.EnumerateAttributesSetup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertServerPolicy::EnumerateAttributesSetup


## -description


The <b>EnumerateAttributesSetup</b> method initializes the internal enumeration pointer to the first request  <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">attribute</a> associated with the current <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">context</a>.


## -parameters




### -param Flags [in]

This parameter is reserved and must be set to zero.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



The 
<a href="https://msdn.microsoft.com/en-us/library/Aa385398(v=VS.85).aspx">SetContext</a> method must be called prior to calling this method. The call to <b>SetContext</b> specifies which request to use as the current context.

To retrieve the attribute, call the <a href="https://msdn.microsoft.com/en-us/library/Aa385081(v=VS.85).aspx">EnumerateAttributes</a> method. The call to <b>EnumerateAttributes</b> retrieves the first attribute and moves the index to the next attribute if one exists.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Set the context. The value nContext (long) would be the same
// as the context parameter in ICertPolicy::VerifyRequest.
// hr is defined as an HRESULT.
// pCertServerPolicy has been used to call SetContext previously.
hr = pCertServerPolicy-&gt;SetContext(nContext);
if (FAILED(hr))
{
    printf("Failed SetContext [%x]\n", hr);
    goto error;
}

// Setup the enumeration.
hr = pCertServerPolicy-&gt;EnumerateAttributesSetup(0);
if (FAILED(hr))
{
    printf("Failed EnumerateAttributesSetup [%x]\n", hr);
    goto error;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa385080(v=VS.85).aspx">ICertServerPolicy</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385081(v=VS.85).aspx">ICertServerPolicy::EnumerateAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385082(v=VS.85).aspx">ICertServerPolicy::EnumerateAttributesClose</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385398(v=VS.85).aspx">ICertServerPolicy::SetContext</a>
 

 

