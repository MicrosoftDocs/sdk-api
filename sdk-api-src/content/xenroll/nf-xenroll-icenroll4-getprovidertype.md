---
UID: NF:xenroll.ICEnroll4.getProviderType
title: ICEnroll4::getProviderType
author: windows-sdk-content
description: Retrieves the type of the specified cryptographic service provider (CSP). This method was first defined in the ICEnroll4 interface.
old-location: security\icenroll4_getprovidertype.htm
tech.root: seccrypto
ms.assetid: f47c07b8-0919-44d4-b331-e062341aa050
ms.author: windowssdkdev
ms.date: 12/04/2018
ms.keywords: CEnroll object [Security],getProviderType method, ICEnroll4 interface [Security],getProviderType method, ICEnroll4.getProviderType, ICEnroll4::getProviderType, getProviderType, getProviderType method [Security], getProviderType method [Security],CEnroll object, getProviderType method [Security],ICEnroll4 interface, security.icenroll4_getprovidertype, xenroll/ICEnroll4::getProviderType
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
 - ICEnroll4.getProviderType
 - CEnroll.getProviderType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll4::getProviderType


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>getProviderType</b> method  retrieves the type of the specified <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP). This method was first defined in the <a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a> interface.


## -parameters




### -param strProvName [in]

A string value that specifies the name of the CSP whose type is being requested.


### -param plProvType [out]

A pointer to <b>LONG</b> value that receives the CSP type. The CSP type is one of the following values.

<ul>
<li>PROV_DH_SCHANNEL</li>
<li>PROV_DSS</li>
<li>PROV_DSS_DH</li>
<li>PROV_FORTEZZA</li>
<li>PROV_MS_EXCHANGE</li>
<li>PROV_RSA_FULL</li>
<li>PROV_RSA_SCHANNEL</li>
<li>PROV_RSA_SIG</li>
<li>PROV_SSL</li>
</ul>

## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 A value that represents the provider type for the provider specified by <i>strProvName</i>. This can be one of the following values.<ul>
<li>PROV_RSA_FULL</li>
<li>PROV_RSA_SIG</li>
<li>PROV_DSS</li>
<li>PROV_FORTEZZA</li>
<li>PROV_MS_EXCHANGE</li>
<li>PROV_SSL</li>
<li>PROV_RSA_SCHANNEL</li>
<li>PROV_DSS_DH</li>
<li>PROV_DH_SCHANNEL</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>
 

 

