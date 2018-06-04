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

# ICEnroll3::get_HashAlgID


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>HashAlgID</b> property sets or retrieves the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash algorithm</a> used when signing a PKCS #10 <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.

This property was first introduced in the <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a> interface.

This property is read/write.


## -parameters


## -remarks



The values for this property are <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash algorithm</a> IDs, such as those returned by the 
<a href="https://msdn.microsoft.com/b7fe4abc-38e8-42a0-a7a0-312ccfc309e5">EnumAlgs</a> method. If both the <b>HashAlgID</b> and 
<a href="https://msdn.microsoft.com/48f8a47b-0ab4-4150-b8cf-37e57fb04d3e">HashAlgorithm</a> properties are set, whichever has been updated most recently determines the hash algorithm used to sign the PKCS #10 request.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Code to set the hash algorithm ID.
// hr is HRESULT variable.
hr = pEnroll-&gt;put_HashAlgID( CALG_MD4 );
if ( FAILED( hr ) )    
    printf("Failed put_HashAlgID [%x]\n", hr);


// Code to retrieve the hash algorithm ID.
DWORD dwHashID;

hr = pEnroll-&gt;get_HashAlgID( &amp;dwHashID );
if ( FAILED( hr ) )    
    printf("Failed get_HashAlgID [%x]\n", hr);
else
    printf("HashAlgID: %d\n", dwHashID);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/b7fe4abc-38e8-42a0-a7a0-312ccfc309e5">EnumAlgs</a>



<a href="https://msdn.microsoft.com/48f8a47b-0ab4-4150-b8cf-37e57fb04d3e">HashAlgorithm</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>
 

 

