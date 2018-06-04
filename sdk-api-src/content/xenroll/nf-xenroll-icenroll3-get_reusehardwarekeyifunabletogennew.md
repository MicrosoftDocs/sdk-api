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

# ICEnroll3::get_ReuseHardwareKeyIfUnableToGenNew


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ReuseHardwareKeyIfUnableToGenNew</b> property sets or retrieves a Boolean value that determines the action taken by the 
certificate enrollment control object if an error is encountered when generating a new key.

This property was first defined in the <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a> interface.

This property is read/write.


## -parameters


## -remarks



This property is a Boolean value. This property affects only <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service providers</a> that return NTE_TOKEN_KEYSET_STORAGE_FULL. These CSPs are typically hardware-based; an example is a smart card. If this property is true and an error is encountered while generating a new key, the certificate enrollment control object will reuse the existing hardware key. If this property is false and an error is encountered while generating a new key, the certificate enrollment control object will not reuse the existing hardware key but will instead pass an error to the caller.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Code to set the reuse H/W key status.
// hr is HRESULT variable.
hr = pEnroll-&gt;put_ReuseHardwareKeyIfUnableToGenNew( FALSE );
if ( FAILED( hr ) )    
    printf("Failed put_ReuseHardwareKeyIfUnableToGenNew [%x]\n", hr);


// Code to retrieve the reuse H/W key status.
BOOL bReuse;

hr = pEnroll-&gt;get_ReuseHardwareKeyIfUnableToGenNew( &amp;bReuse );
if ( FAILED( hr ) )
    printf("Failed get_ReuseHardwareKeyIfUnableToGenNew [%x]\n", hr);
else
    printf("Hardware key %s be reused if unable"
        " to generate a new key.\n", bReuse ? "will" : "will not");</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>
 

 

