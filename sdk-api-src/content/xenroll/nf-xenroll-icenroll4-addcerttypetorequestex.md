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

# ICEnroll4::addCertTypeToRequestEx


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addCertTypeToRequestEx</b>  method, like the 
<a href="https://msdn.microsoft.com/d2c22689-d386-43d1-a42f-f303a034a087">addCertTypeToRequest</a> method, adds a certificate template (or "certificate type") to a request. This method was first defined in the <a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a> interface.

This method is associated with the Certificate Services enterprise 
<a href="https://msdn.microsoft.com/23d920ea-af62-42ce-ad48-c7a03ab55fc9">policy module</a>. This method is specialized, and its use is not recommended for most applications. This version can add a V@ template extension into a request.


## -parameters




### -param lType




### -param bstrOIDOrName [in]

The certificate template fully qualified name which is being added to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. This value is interpreted by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a>.


### -param lMajorVersion [in]

Sets the major version of the template. This parameter is ignored if <i>lFlag</i> is XECT_EXTENSION_V!.


### -param fMinorVersion [in]

Indicates whether a minor version of the template is used. This parameter is ignored if <i>lFlag</i> is XECT_EXTENSION_V!.


### -param lMinorVersion [in]

Sets the minor version of the template. This parameter is ignored if <i>lFlag</i> is XECT_EXTENSION_V1 or if <i>fMinorVersion</i> is <b>FALSE</b>.


#### - lFlag [in]

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
 

 

