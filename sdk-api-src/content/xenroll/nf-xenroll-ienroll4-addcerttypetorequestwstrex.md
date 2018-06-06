---
UID: NF:xenroll.IEnroll4.AddCertTypeToRequestWStrEx
title: IEnroll4::AddCertTypeToRequestWStrEx
author: windows-sdk-content
description: Adds a certificate template (also known as certificate type) to a request.
old-location: security\ienroll4_addcerttypetorequestwstrex.htm
old-project: SecCrypto
ms.assetid: aa3bab0d-2ed4-4ef2-9665-a6c70e14308d
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: AddCertTypeToRequestWStrEx, AddCertTypeToRequestWStrEx method [Security], AddCertTypeToRequestWStrEx method [Security],IEnroll4 interface, IEnroll4 interface [Security],AddCertTypeToRequestWStrEx method, IEnroll4.AddCertTypeToRequestWStrEx, IEnroll4::AddCertTypeToRequestWStrEx, XECT_EXTENSION_V1, XECT_EXTENSION_V2, security.ienroll4_addcerttypetorequestwstrex, xenroll/IEnroll4::AddCertTypeToRequestWStrEx
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
 - IEnroll4.AddCertTypeToRequestWStrEx
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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
 

 

