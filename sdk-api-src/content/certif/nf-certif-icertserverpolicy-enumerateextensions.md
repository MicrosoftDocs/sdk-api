---
UID: NF:certif.ICertServerPolicy.EnumerateExtensions
title: ICertServerPolicy::EnumerateExtensions
author: windows-sdk-content
description: Retrieves the object identifier (OID) of the current extension and moves the internal enumeration pointer to the next extension.
old-location: security\icertserverpolicy_enumerateextensions.htm
tech.root: seccrypto
ms.assetid: 565ff4d5-0d22-466d-8458-f98b992a1868
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CCertServerPolicy object [Security],EnumerateExtensions method, EnumerateExtensions, EnumerateExtensions method [Security], EnumerateExtensions method [Security],CCertServerPolicy object, EnumerateExtensions method [Security],ICertServerPolicy interface, ICertServerPolicy interface [Security],EnumerateExtensions method, ICertServerPolicy.EnumerateExtensions, ICertServerPolicy::EnumerateExtensions, _certsrv_icertserverpolicy_enumerateextensions, certif/ICertServerPolicy::EnumerateExtensions, security.icertserverpolicy_enumerateextensions
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
 - ICertServerPolicy.EnumerateExtensions
 - CCertServerPolicy.EnumerateExtensions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertServerPolicy::EnumerateExtensions


## -description


The <b>EnumerateExtensions</b> method retrieves the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the current extension and moves the internal enumeration pointer to the next  extension.


## -parameters




### -param pstrExtensionName [out]

A pointer to a <b>BSTR</b> that contains the OID of the current extension.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and the <i>pstrExtensionName</i> parameter contains the OID  of the current extension. A value of S_FALSE is returned if the last extension was already enumerated.

To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrExtensionName</i>.

When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a string that contains the OID of the extension, or an empty string if the last extension was already enumerated.




## -remarks



This method enumerates certificate extensions recorded in the database, even those that are disabled and do not appear in the certificate. To determine whether an extension is disabled, use 
<a href="https://msdn.microsoft.com/6266e96d-81da-478f-99da-86936b4cfc6b">GetCertificateExtensionFlags</a> to test the extension's EXTENSION_DISABLE_FLAG bit.

When done enumerating, call the <a href="https://msdn.microsoft.com/b1755fc5-f18f-45b5-a89a-44c6598c0e2c">EnumerateExtensionsClose</a> method to free resources used by the enumeration calls.


#### Examples

<pre class="syntax" xml:space="preserve"><code>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;Certif.h&gt;

BSTR     bstrExt = NULL;
VARIANT  varExt;
LONG     ExtFlags;
HRESULT  hr;

VariantInit(&amp;varExt);

// Enumerate the extensions.
while (S_OK ==
      (hr = pCertServerPol-&gt;EnumerateExtensions(&amp;bstrExt)))
{
  // Retrieve the extension data.
  if (FAILED(pCertServerPol-&gt;GetCertificateExtension(
                             bstrExt,
                             PROPTYPE_BINARY,
                             &amp;varExt)))
      printf("Failed GetCertificateExtension\n");
  else
  {
     // Retrieve the extension flags.
    if (FAILED(pCertServerPol-&gt;GetCertificateExtensionFlags(
                               &amp;ExtFlags)))
        printf("Failed GetCertificateExtensionFlags\n");
    else
        // This sample will display the extension OID string,
        // the extension flags (in hex) and
        // the length of the BSTR binary ASN-encode extension.
        printf("Extension: %ws\tFlags:%x\tLength:%u\n",
               bstrExt,
               ExtFlags,
               SysStringByteLen(varExt.bstrVal));
  }
}
// Determine if hr was S_FALSE, meaning the enumeration 
// was completed, or some other error.
if (S_FALSE != hr)
    printf("Failed EnumerateExtensions - %x\n", hr);
// Free BSTR resource.
if (NULL != bstrExt)
    SysFreeString(bstrExt);
// Free VARIANT resource.
    VariantClear(&amp;varExt);
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/b1755fc5-f18f-45b5-a89a-44c6598c0e2c">EnumerateExtensionsClose</a>



<a href="https://msdn.microsoft.com/e7ad32a5-d7df-407f-8efe-c9931610c2d2">EnumerateExtensionsSetup</a>



<a href="https://msdn.microsoft.com/e2c8e1d5-6ddb-4c8f-8052-f45cd52e2bef">GetCertificateExtension</a>



<a href="https://msdn.microsoft.com/6266e96d-81da-478f-99da-86936b4cfc6b">GetCertificateExtensionFlags</a>



<a href="https://msdn.microsoft.com/7d16161e-9827-46a0-9989-30ebca792bb1">ICertServerPolicy</a>
 

 

