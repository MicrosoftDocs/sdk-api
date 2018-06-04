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

# ICEnroll2::addNameValuePairToSignature


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addNameValuePairToSignature</b> method 
			adds the authenticated name-value pair of an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a> to the request. It is up to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) to interpret the meaning of the name-value pair.
		 This method was first defined in the <a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a> interface.


## -parameters




### -param Name [in]

The name of the attribute, such as "2.5.4.6" for the country/region name.


### -param Value [in]

The value of the attribute, such as "US".


## -returns



<h3>VB</h3>
 The return value is an <b>HRESULT</b>, with <b>S_OK</b> returned if the call is successful.




## -remarks



The <b>addNameValuePairToSignature</b> method is used  to add attributes to the request.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BSTR bstrName = NULL;
BSTR bstrValue = NULL;
HRESULT hr;

// Allocate the name. Alternatively, (L"2.5.4.6").
bstrName = SysAllocString(TEXT(szOID_COUNTRY_NAME));
// Allocate the value.
bstrValue = SysAllocString(L"US");

if (NULL == bstrName || NULL == bstrValue)
{
    // handle error
}

// add the name-value pair to the signature
// pEnroll is previously instantiated ICEnroll4 interface pointer
hr = pEnroll-&gt;addNameValuePairToSignature( bstrName, bstrValue );
if ( FAILED( hr ) )
    printf("Failed addNameValuePairToSignature - %x\n", hr );
else
    printf("addNameValuePairToSignature(%ws, %ws) succeeded\n",
            bstrName, 
            bstrValue );

// free BSTRs
if (bstrName )
    SysFreeString( bstrName );
if (bstrValue )
    SysFreeString( bstrValue );</pre>
</td>
</tr>
</table></span></div>


