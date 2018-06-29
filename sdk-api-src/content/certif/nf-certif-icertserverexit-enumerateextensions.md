---
UID: NF:certif.ICertServerExit.EnumerateExtensions
title: ICertServerExit::EnumerateExtensions
author: windows-sdk-content
description: Returns the object identifier (OID) string (also known as the extension name) of the next certificate extension to be enumerated, then increments the internal pointer to the following extension.
old-location: security\icertserverexit_enumerateextensions.htm
old-project: SecCrypto
ms.assetid: 8726f5fa-dc85-4357-b73a-013842d6ab78
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CCertServerExit object [Security],EnumerateExtensions method, EnumerateExtensions, EnumerateExtensions method [Security], EnumerateExtensions method [Security],CCertServerExit object, EnumerateExtensions method [Security],ICertServerExit interface, ICertServerExit interface [Security],EnumerateExtensions method, ICertServerExit.EnumerateExtensions, ICertServerExit::EnumerateExtensions, _certsrv_icertserverexit_enumerateextensions, certif/ICertServerExit::EnumerateExtensions, security.icertserverexit_enumerateextensions
ms.prod: windows
ms.technology: windows-sdk
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
 - ICertServerExit.EnumerateExtensions
 - CCertServerExit.EnumerateExtensions
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
---

# ICertServerExit::EnumerateExtensions


## -description


The <b>EnumerateExtensions</b> method returns the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) string (also known as the extension name) of the next certificate extension to be enumerated, then increments the internal pointer to the following extension.

 Before calling <b>EnumerateExtensions</b>, an application calls 
<a href="https://msdn.microsoft.com/2a0c4919-b3a0-4027-85bd-970f6bc0cdeb">ICertServerExit::EnumerateExtensionsSetup</a>. When done enumerating, an application calls 
<a href="https://msdn.microsoft.com/769235cd-d5ef-458b-a04b-88f9f831ce3f">ICertServerExit::EnumerateExtensionsClose</a>.


## -parameters




### -param pstrExtensionName [out]

A pointer to the enumerated extension name.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and *<i>pstrExtensionName</i> is set to the <b>BSTR</b> that contains the name of the enumerated extension. A value of S_FALSE is returned if the last extension was already enumerated.

To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrExtensionName</i>.

When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a string that contains the name of the enumerated extension, or an empty string if the last extension was already enumerated.




## -remarks



This method enumerates certificate extensions recorded in the database, even those that are disabled and do not appear in the certificate. To determine whether an extension is disabled, use 
<a href="https://msdn.microsoft.com/0eee1d67-116b-4f93-9273-b70d50fa2c5d">ICertServerExit::GetCertificateExtensionFlags</a> to test the extension's EXTENSION_DISABLE_FLAG bit.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BSTR     bstrExt = NULL;
VARIANT  varExt;
LONG     ExtFlags;
HRESULT  hr;

VariantInit(&amp;varExt);

// Enumerate the extensions.
while (S_OK ==
      (hr = pCertServerExit-&gt;EnumerateExtensions(&amp;bstrExt)))
{
  // Retrieve the extension data.
  if (FAILED(pCertServerExit-&gt;GetCertificateExtension(
                              bstrExt,
                              PROPTYPE_BINARY,
                              &amp;varExt)))
      printf("Failed GetCertificateExtension\n");
  else
  {
     // Retrieve the extension flags.
    if (FAILED(pCertServerExit-&gt;GetCertificateExtensionFlags(
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
    VariantClear(&amp;varExt);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1554c09c-a7c1-44ad-9821-93c0913212fc">ICertServerExit</a>



<a href="https://msdn.microsoft.com/769235cd-d5ef-458b-a04b-88f9f831ce3f">ICertServerExit::EnumerateExtensionsClose</a>



<a href="https://msdn.microsoft.com/2a0c4919-b3a0-4027-85bd-970f6bc0cdeb">ICertServerExit::EnumerateExtensionsSetup</a>



<a href="https://msdn.microsoft.com/ba2d2e5f-230e-4e69-8d86-dad9c743e5ee">ICertServerExit::GetCertificateExtension</a>



<a href="https://msdn.microsoft.com/0eee1d67-116b-4f93-9273-b70d50fa2c5d">ICertServerExit::GetCertificateExtensionFlags</a>
 

 

