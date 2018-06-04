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

# ICEnroll3::EnumAlgs


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>EnumAlgs</b> method retrieves the IDs of cryptographic algorithms in a given algorithm class that are supported by the current <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP).  This method was first defined in the <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a> interface.


## -parameters




### -param dwIndex [in]

Specifies the ordinal position of the algorithm whose ID will be retrieved. Specify zero for the first algorithm.


### -param algClass [in]

A cryptographic algorithm class. The IDs returned by this method will be in the specified class. Specify one of the following:

<ul>
<li>ALG_CLASS_HASH</li>
<li>ALG_CLASS_KEY_EXCHANGE</li>
<li>ALG_CLASS_MSG_ENCRYPT</li>
<li>ALG_CLASS_DATA_ENCRYPT</li>
<li>ALG_CLASS_SIGNATURE</li>
</ul>

### -param pdwAlgID [out]

A pointer to a variable to receive a cryptographic algorithm ID that is supported by the current CSP.


## -returns



<h3>C++</h3>
 The return value is an <b>HRESULT</b>. A value of S_OK indicates success. When there are no more algorithms to enumerate, the value ERROR_NO_MORE_ITEMS is returned.

<h3>VB</h3>
 A cryptographic algorithm ID which is supported by the current CSP. When there are no more algorithms to enumerate, the value ERROR_NO_MORE_ITEMS is returned.




## -remarks



For algorithm ID and class constants used by this method, see Wincrypt.h.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;Xenroll.h&gt;

DWORD     dwAlgID;
DWORD     dwIndex;

BSTR      bstrAlgName = NULL;

HRESULT   hr, hr2;

// Loop through the AlgIDs.
dwIndex = 0;
while ( TRUE )
{
    // Enumerate the alg IDs for a specific class.
    hr = pEnroll-&gt;EnumAlgs(dwIndex, ALG_CLASS_SIGNATURE, &amp;dwAlgID);
    if ( S_OK != hr )
    {
       break;
    }

    // Do something with the AlgID.
    // For example, retrieve the corresponding name.
    hr2 = pEnroll-&gt;GetAlgName( dwAlgID, &amp;bstrAlgName);
    if ( FAILED( hr2 ) )    
        printf("Failed GetAlgName [%x]\n", hr);
    else
        printf("AlgID: %d Name: %S\n", dwAlgID, bstrAlgName );

    // Reuse the BSTR variable in next iteration.
    if ( NULL != bstrAlgName )
    {
        SysFreeString( bstrAlgName );
        bstrAlgName = NULL;
    }

    // Increment the index.
    dwIndex++;
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>
 

 

