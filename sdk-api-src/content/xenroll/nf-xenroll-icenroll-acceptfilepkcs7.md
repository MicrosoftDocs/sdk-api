---
UID: NF:xenroll.ICEnroll.acceptFilePKCS7
title: ICEnroll::acceptFilePKCS7
author: windows-sdk-content
description: Accepts and processes a file that contains a PKCS #7 message containing a certificate. This method was first defined in the ICEnroll interface.
old-location: security\icenroll4_acceptfilepkcs7.htm
tech.root: SecCrypto
ms.assetid: dae9f6b8-6690-47cc-9397-168c1ff54c55
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CEnroll object [Security],acceptFilePKCS7 method, ICEnroll interface [Security],acceptFilePKCS7 method, ICEnroll.acceptFilePKCS7, ICEnroll2 interface [Security],acceptFilePKCS7 method, ICEnroll2::acceptFilePKCS7, ICEnroll3 interface [Security],acceptFilePKCS7 method, ICEnroll3::acceptFilePKCS7, ICEnroll4 interface [Security],acceptFilePKCS7 method, ICEnroll4::acceptFilePKCS7, ICEnroll::acceptFilePKCS7, acceptFilePKCS7, acceptFilePKCS7 method [Security], acceptFilePKCS7 method [Security],CEnroll object, acceptFilePKCS7 method [Security],ICEnroll interface, acceptFilePKCS7 method [Security],ICEnroll2 interface, acceptFilePKCS7 method [Security],ICEnroll3 interface, acceptFilePKCS7 method [Security],ICEnroll4 interface, security.icenroll4_acceptfilepkcs7, xenroll/ICEnroll2::acceptFilePKCS7, xenroll/ICEnroll3::acceptFilePKCS7, xenroll/ICEnroll4::acceptFilePKCS7, xenroll/ICEnroll::acceptFilePKCS7
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.acceptFilePKCS7
 - ICEnroll3.acceptFilePKCS7
 - ICEnroll2.acceptFilePKCS7
 - ICEnroll.acceptFilePKCS7
 - CEnroll.acceptFilePKCS7
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::acceptFilePKCS7


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>acceptFilePKCS7</b> method accepts and processes a file that contains a PKCS #7 message containing a certificate. This method was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.


## -parameters




### -param wszPKCS7FileName [in]

Specifies the name of the file that contains the PKCS #7 message.


## -returns



<h3>VB</h3>
The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Upon successful completion of this function, the PKCS #7 message in the file will be accepted.




## -remarks




By default, the My, Ca, Root, and Request system stores are used to store the certificates. However, you can specify other stores by assigning the following properties before calling this method:

<ul>
<li>
<a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">MyStoreName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">CAStoreName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">RootStoreName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">RequestStoreName</a>
</li>
</ul>


The <b>acceptFilePKCS7</b> method differs from 
<a href="https://msdn.microsoft.com/5a428d83-c846-4f44-a682-58c3e025c353">acceptPKCS7</a> only in that a file supplies the certificate.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT  hr;
BSTR     bstrFileName;

// Allocate a BSTR referencing an existing file, 
// for example, "myPKCS7.fil".
bstrFileName = SysAllocString(TEXT("&lt;FILENAMEHERE&gt;"));
if (NULL == bstrFileName)
{
    //handle error
}

// pEnroll is a previously instantiated ICEnroll interface pointer.
hr = pEnroll-&gt;acceptFilePKCS7( bstrFileName );
if (FAILED(hr))
    printf("Failed acceptFilePKCS7 - %x\n", hr );
else
	printf("Accepted PKCS #7 from file %ws successfully\n", 
	bstrFileName );

// Free BSTR when done.
if (bstrFileName)
    SysFreeString(bstrFileName);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/29616175-7195-430e-a85b-99b50e276e7f">CAStoreName</a>



<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>



<a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>



<a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">MyStoreName</a>



<a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">RequestStoreName</a>



<a href="https://msdn.microsoft.com/5b686ade-e8ee-4c59-ab90-05088f575acd">RootStoreName</a>



<a href="https://msdn.microsoft.com/5a428d83-c846-4f44-a682-58c3e025c353">acceptPKCS7</a>
 

 

