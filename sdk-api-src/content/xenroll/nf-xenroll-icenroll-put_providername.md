---
UID: NF:xenroll.ICEnroll.put_ProviderName
title: ICEnroll::put_ProviderName
author: windows-sdk-content
description: The ProviderName property of ICEnroll4 sets or retrieves the name of the cryptographic service provider (CSP) to use.
old-location: security\icenroll4_providername.htm
tech.root: SecCrypto
ms.assetid: 092d5ed1-8d03-45d8-bc7a-3e27035f4b2f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CEnroll object [Security],ProviderName property, ICEnroll interface [Security],ProviderName property, ICEnroll.ProviderName, ICEnroll.put_ProviderName, ICEnroll2 interface [Security],ProviderName property, ICEnroll2.ProviderName, ICEnroll2::get_ProviderName, ICEnroll2::put_ProviderName, ICEnroll3 interface [Security],ProviderName property, ICEnroll3.ProviderName, ICEnroll3::get_ProviderName, ICEnroll3::put_ProviderName, ICEnroll4 interface [Security],ProviderName property, ICEnroll4.ProviderName, ICEnroll4::ProviderName, ICEnroll4::get_ProviderName, ICEnroll4::put_ProviderName, ICEnroll::get_ProviderName, ICEnroll::put_ProviderName, ProviderName property [Security], ProviderName property [Security],CEnroll object, ProviderName property [Security],ICEnroll interface, ProviderName property [Security],ICEnroll2 interface, ProviderName property [Security],ICEnroll3 interface, ProviderName property [Security],ICEnroll4 interface, put_ProviderName, security.icenroll4_providername, xenroll/ICEnroll2::ProviderName, xenroll/ICEnroll2::get_ProviderName, xenroll/ICEnroll2::put_ProviderName, xenroll/ICEnroll3::ProviderName, xenroll/ICEnroll3::get_ProviderName, xenroll/ICEnroll3::put_ProviderName, xenroll/ICEnroll4::ProviderName, xenroll/ICEnroll4::get_ProviderName, xenroll/ICEnroll4::put_ProviderName, xenroll/ICEnroll::ProviderName, xenroll/ICEnroll::get_ProviderName, xenroll/ICEnroll::put_ProviderName
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
 - ICEnroll4.ProviderName
 - ICEnroll4.get_ProviderName
 - ICEnroll4.put_ProviderName
 - ICEnroll3.ProviderName
 - ICEnroll3.get_ProviderName
 - ICEnroll3.put_ProviderName
 - ICEnroll2.ProviderName
 - ICEnroll2.get_ProviderName
 - ICEnroll2.put_ProviderName
 - ICEnroll.ProviderName
 - ICEnroll.get_ProviderName
 - ICEnroll.put_ProviderName
 - CEnroll.ProviderName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::put_ProviderName


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ProviderName</b> property sets or retrieves the name of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) to use.

If the CSP has not been specified, the default value for this property  is "Microsoft Base Cryptographic Provider", and the <b>ProviderName</b> property is set to an empty string. This property was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>ProviderName</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/b8e841c1-f16e-4f3a-94f2-ef6708c88910">createPKCS10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/074c7321-6117-4261-836a-a2055c9e029d">createFilePKCS10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/28102a55-3bda-4413-84b6-cfa2057be98b">enumContainers</a>
</li>
</ul>



#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BSTR     bstrProvName = NULL;
BSTR     bstrMyProvName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the ProviderName
hr = pEnroll->get_ProviderName( &bstrProvName );
if (FAILED( hr ))
    printf("Failed get_ProviderName - %x\n", hr );
else
    printf( "ProviderName: %ws\n", bstrProvName );
// free BSTR when done
if ( NULL != bstrProvName )
    SysFreeString( bstrProvName );

// set the ProviderName value
bstrMyProvName = SysAllocString(TEXT("Microsoft Base DSS")
                                TEXT(" Cryptographic Provider"));
hr = pEnroll->put_ProviderName( bstrMyProvName );
if (FAILED( hr ))
    printf("Failed put_ProviderName - %x\n", hr );
else
    printf( "ProviderName set to %ws\n", bstrMyProvName );
// free BSTR when done
if ( NULL != bstrMyProvName )
    SysFreeString( bstrMyProvName );</pre>
</td>
</tr>
</table></span></div>




