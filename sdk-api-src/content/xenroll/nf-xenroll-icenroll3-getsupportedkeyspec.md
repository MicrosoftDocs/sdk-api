---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

