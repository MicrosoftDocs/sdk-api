---
UID: NF:xenroll.ICEnroll2.addNameValuePairToSignature
title: ICEnroll2::addNameValuePairToSignature
author: windows-sdk-content
description: Adds the authenticated name-value pair of an attribute to the request. It is up to the certification authority (CA) to interpret the meaning of the name-value pair.
old-location: security\icenroll4_addnamevaluepairtosignature.htm
old-project: SecCrypto
ms.assetid: a31975f7-432e-47bb-a24e-508c6ca85373
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CEnroll object [Security],addNameValuePairToSignature method, ICEnroll2 interface [Security],addNameValuePairToSignature method, ICEnroll2.addNameValuePairToSignature, ICEnroll2::addNameValuePairToSignature, ICEnroll3 interface [Security],addNameValuePairToSignature method, ICEnroll3::addNameValuePairToSignature, ICEnroll4 interface [Security],addNameValuePairToSignature method, ICEnroll4::addNameValuePairToSignature, addNameValuePairToSignature, addNameValuePairToSignature method [Security], addNameValuePairToSignature method [Security],CEnroll object, addNameValuePairToSignature method [Security],ICEnroll2 interface, addNameValuePairToSignature method [Security],ICEnroll3 interface, addNameValuePairToSignature method [Security],ICEnroll4 interface, security.icenroll4_addnamevaluepairtosignature, xenroll/ICEnroll2::addNameValuePairToSignature, xenroll/ICEnroll3::addNameValuePairToSignature, xenroll/ICEnroll4::addNameValuePairToSignature
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
 - ICEnroll4.addNameValuePairToSignature
 - ICEnroll3.addNameValuePairToSignature
 - ICEnroll2.addNameValuePairToSignature
 - CEnroll.addNameValuePairToSignature
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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


