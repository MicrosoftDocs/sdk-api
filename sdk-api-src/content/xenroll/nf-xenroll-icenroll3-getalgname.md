---
UID: NF:xenroll.ICEnroll3.GetAlgName
title: ICEnroll3::GetAlgName
author: windows-sdk-content
description: Retrieves the name of a cryptographic algorithm given its ID. The values retrieved by this method depend on the current cryptographic service provider (CSP). This method was first defined in the ICEnroll3 interface.
old-location: security\icenroll4_getalgname.htm
tech.root: seccrypto
ms.assetid: 9c5fa25c-7fab-4fb5-9ff6-bc7379260926
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CEnroll object [Security],GetAlgName method, GetAlgName, GetAlgName method [Security], GetAlgName method [Security],CEnroll object, GetAlgName method [Security],ICEnroll3 interface, GetAlgName method [Security],ICEnroll4 interface, ICEnroll3 interface [Security],GetAlgName method, ICEnroll3.GetAlgName, ICEnroll3::GetAlgName, ICEnroll4 interface [Security],GetAlgName method, ICEnroll4::GetAlgName, security.icenroll4_getalgname, xenroll/ICEnroll3::GetAlgName, xenroll/ICEnroll4::GetAlgName
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICEnroll4.GetAlgName
 - ICEnroll3.GetAlgName
 - CEnroll.GetAlgName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll3::GetAlgName


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GetAlgName</b> method retrieves the name of a cryptographic algorithm given its ID. The values retrieved by this method depend on the current <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP). This method was first defined in the <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a> interface.


## -parameters




### -param algID [in]

A value that represents a cryptographic algorithm, as defined in Wincrypt.h. For example, CALG_MD2 is a defined algorithm identifier. For this method to be successful, the current CSP must support the <i>algID</i> algorithm.


### -param pbstr [out]

Upon success, a pointer to a <b>BSTR</b> that represents the name of the algorithm specified by <i>algID</i>. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 The return value is an <b>HRESULT</b>. A value of S_OK indicates success. If a CSP does not support this method or does not support the <i>algID</i> cryptographic algorithm, an error is returned.

<h3>VB</h3>
 The return value is a string that represents the name of the algorithm specified by <i>algID</i>. If a CSP does not support this method, an error is returned.




## -remarks



This method may be used to display the names of algorithms whose IDs are retrieved by calling 
<a href="https://msdn.microsoft.com/b7fe4abc-38e8-42a0-a7a0-312ccfc309e5">EnumAlgs</a>.

Constants for the cryptographic algorithms are defined in Wincrypt.h.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BSTR      bstrAlgName = NULL;

HRESULT   hr;

// Retrieve the algorithm name.
// dwAlgID is a DWORD variable for an algorithm ID.
hr = pEnroll-&gt;GetAlgName( dwAlgID, &amp;bstrAlgName);
if (FAILED(hr))
    printf("Failed GetAlgName [%x]\n", hr);
else
    printf("AlgID: %d Name: %S\n", dwAlgID, bstrAlgName );

// Free BSTR resource.
if ( NULL != bstrAlgName )
{
    SysFreeString( bstrAlgName );
    bstrAlgName = NULL;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/b7fe4abc-38e8-42a0-a7a0-312ccfc309e5">EnumAlgs</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>
 

 

