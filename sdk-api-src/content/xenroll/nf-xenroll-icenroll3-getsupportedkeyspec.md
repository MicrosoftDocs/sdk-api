---
UID: NF:xenroll.ICEnroll3.GetSupportedKeySpec
title: ICEnroll3::GetSupportedKeySpec
author: windows-sdk-content
description: Retrieves information regarding the current cryptographic service provider (CSP) support for signature and/or exchange operations. This method was first defined in the ICEnroll3 interface.
old-location: security\icenroll4_getsupportedkeyspec.htm
old-project: seccrypto
ms.assetid: e225eddb-0c36-446a-9696-38653ff22511
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CEnroll object [Security],GetSupportedKeySpec method, GetSupportedKeySpec, GetSupportedKeySpec method [Security], GetSupportedKeySpec method [Security],CEnroll object, GetSupportedKeySpec method [Security],ICEnroll3 interface, GetSupportedKeySpec method [Security],ICEnroll4 interface, ICEnroll3 interface [Security],GetSupportedKeySpec method, ICEnroll3.GetSupportedKeySpec, ICEnroll3::GetSupportedKeySpec, ICEnroll4 interface [Security],GetSupportedKeySpec method, ICEnroll4::GetSupportedKeySpec, security.icenroll4_getsupportedkeyspec, xenroll/ICEnroll3::GetSupportedKeySpec, xenroll/ICEnroll4::GetSupportedKeySpec
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.GetSupportedKeySpec
 - ICEnroll3.GetSupportedKeySpec
 - CEnroll.GetSupportedKeySpec
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# ICEnroll3::GetSupportedKeySpec


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GetSupportedKeySpec</b> method retrieves information regarding the current <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) support for signature and/or exchange operations. This method was first defined in the <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a> interface.

The values retrieved by this method are dependent upon the current CSP.


## -parameters




### -param pdwKeySpec [out]

A pointer to a <b>LONG</b> that receives a bit flag that indicates whether the current CSP supports <a href="https://msdn.microsoft.com/library/windows/hardware/mt764003">exchange</a> and <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">signature keys</a>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a value that indicates whether the current CSP supports exchange and signature keys. If the CSP does not support this method, an error is returned.




## -remarks



Call this method to determine whether the current CSP supports exchange keys, signature keys, or both. The <i>pdwKeySpec</i> parameter will contain one or more of the following constants (defined in in Wincrypt.h):<ul>
<li>AT_KEYEXCHANGE</li>
<li>AT_SIGNATURE</li>
</ul>



#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DWORD dwKeySpec;

// Determine the supported key specifications.
// hr is HRESULT variable.
hr = pEnroll-&gt;GetSupportedKeySpec( &amp;dwKeySpec );
if ( FAILED( hr ) )    
    printf("Failed GetSupportedKeySpec [%x]\n", hr);
else
{
    printf("Exchange keys are %s. Signature keys are %s.\n",
           dwKeySpec &amp; AT_KEYEXCHANGE ? "supported" : "not supported",
           dwKeySpec &amp; AT_SIGNATURE ? "supported" : "not supported" );
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>
 

 

