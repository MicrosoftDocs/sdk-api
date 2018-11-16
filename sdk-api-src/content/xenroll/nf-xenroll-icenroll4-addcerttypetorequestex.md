---
UID: NF:xenroll.ICEnroll4.addCertTypeToRequestEx
title: ICEnroll4::addCertTypeToRequestEx
author: windows-sdk-content
description: Adds a certificate template (or &#0034;certificate type&#0034;) to a request.
old-location: security\icenroll4_addcerttypetorequestex.htm
tech.root: SecCrypto
ms.assetid: bde35e01-8b26-44f7-828e-e8313a2b5a12
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CEnroll object [Security],addCertTypeToRequestEx method, ICEnroll4 interface [Security],addCertTypeToRequestEx method, ICEnroll4.addCertTypeToRequestEx, ICEnroll4::addCertTypeToRequestEx, XECT_EXTENSION_V1, XECT_EXTENSION_V2, _xen_icenroll4_addcerttypetorequestex, addCertTypeToRequestEx, addCertTypeToRequestEx method [Security], addCertTypeToRequestEx method [Security],CEnroll object, addCertTypeToRequestEx method [Security],ICEnroll4 interface, security.icenroll4_addcerttypetorequestex, xenroll/ICEnroll4::addCertTypeToRequestEx
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
 - ICEnroll4.addCertTypeToRequestEx
 - CEnroll.addCertTypeToRequestEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xenroll.h
: 
- ICEnroll4.addCertTypeToRequestEx
: 
---

# ICEnroll4::addCertTypeToRequestEx


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addCertTypeToRequestEx</b>  method, like the 
<a href="https://msdn.microsoft.com/d2c22689-d386-43d1-a42f-f303a034a087">addCertTypeToRequest</a> method, adds a certificate template (or "certificate type") to a request. This method was first defined in the <a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a> interface.

This method is associated with the Certificate Services enterprise 
<a href="https://msdn.microsoft.com/23d920ea-af62-42ce-ad48-c7a03ab55fc9">policy module</a>. This method is specialized, and its use is not recommended for most applications. This version can add a V@ template extension into a request.


## -parameters




### -param lType [in]

Indicates the version type of the template extension. This can be either of the following values: 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XECT_EXTENSION_V1"></a><a id="xect_extension_v1"></a><dl>
<dt><b>XECT_EXTENSION_V1</b></dt>
</dl>
</td>
<td width="60%">
Uses a version 1 extension

</td>
</tr>
<tr>
<td width="40%"><a id="XECT_EXTENSION_V2"></a><a id="xect_extension_v2"></a><dl>
<dt><b>XECT_EXTENSION_V2</b></dt>
</dl>
</td>
<td width="60%">
Uses a version 2 extension

</td>
</tr>
</table>
 


### -param bstrOIDOrName [in]

The certificate template fully qualified name which is being added to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. This value is interpreted by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a>.


### -param lMajorVersion [in]

Sets the major version of the template. This parameter is ignored if <i>lFlag</i> is XECT_EXTENSION_V!.


### -param fMinorVersion [in]

Indicates whether a minor version of the template is used. This parameter is ignored if <i>lFlag</i> is XECT_EXTENSION_V!.


### -param lMinorVersion [in]

Sets the minor version of the template. This parameter is ignored if <i>lFlag</i> is XECT_EXTENSION_V1 or if <i>fMinorVersion</i> is <b>FALSE</b>.


## -returns



<h3>VB</h3>
 The return value is an <b>HRESULT</b>, with <b>S_OK</b> returned if the call is successful.




## -remarks



This method supports only the new request method, 
<a href="https://msdn.microsoft.com/d2a1c1c4-dbbf-423c-bf59-da0ab9a71078">createRequest</a>. It does not support the 
<a href="https://msdn.microsoft.com/b8e841c1-f16e-4f3a-94f2-ef6708c88910">createPKCS10</a> method.

This method can be called multiple times to establish multiple certificate templates for the request.




## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/d2c22689-d386-43d1-a42f-f303a034a087">ICEnroll2::addCertTypeToRequest</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>



<a href="https://msdn.microsoft.com/d2a1c1c4-dbbf-423c-bf59-da0ab9a71078">ICEnroll4::createRequest</a>



<a href="https://msdn.microsoft.com/b8e841c1-f16e-4f3a-94f2-ef6708c88910">ICEnroll::createPKCS10</a>
 

 

