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

# IEnroll4::AddCertTypeToRequestWStrEx


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>AddCertTypeToRequestWStrEx</b> method, like the 
<a href="https://msdn.microsoft.com/d9bf51db-375e-4230-953c-d9893228d7e1">AddCertTypeToRequestWStr</a> method, adds a certificate template (also known as certificate type) to a request.

This method is associated with the Certificate Services enterprise 
<a href="https://msdn.microsoft.com/23d920ea-af62-42ce-ad48-c7a03ab55fc9">policy module</a>. This method is specialized, and its use is not recommended for most applications. This version can add a V2 template extension into a request. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param lType [in]

Indicates the version type of the template extension. It can be either of the following values.

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
 


### -param pwszOIDOrName [in]

A pointer to a null-terminated character string that represents the fully qualified name of the certificate template that is being added to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. This value is interpreted by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a>.


### -param lMajorVersion [in]

Value that specifies the major version of the template. This parameter is ignored if <i>lType</i> is XECT_EXTENSION_V1.


### -param fMinorVersion [in]

Value that specifies whether a minor version of the template is used. This parameter is ignored if <i>lType</i> is XECT_EXTENSION_V1.


### -param lMinorVersion [in]

Value that specifies the minor version of the template. This parameter is ignored if <i>lType</i> is XECT_EXTENSION_V1 or if <i>fMinorVersion</i> is <b>FALSE</b>.


## -returns



The return value is an <b>HRESULT</b>, with S_OK returned if the call is successful.




## -remarks



This method supports only the new request method, 
<a href="https://msdn.microsoft.com/bc2b875c-96f8-453e-8f72-f9032d5aa773">createRequestWStr</a>. It does not support the 
<a href="https://msdn.microsoft.com/ebbcc9ad-9f87-4abe-963b-38c57a60e45e">createPKCS10WStr</a> method.

This method can be called multiple times to establish multiple certificate templates for the request.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

