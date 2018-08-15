---
UID: NF:xenroll.IEnroll4.createRequestWStr
title: IEnroll4::createRequestWStr
author: windows-sdk-content
description: Creates a PKCS #10, PKCS #7, or full Certificate Management over CMS (CMC) format certificate request and stores it in a BLOB.
old-location: security\ienroll4_createrequestwstr.htm
old-project: seccrypto
ms.assetid: bc2b875c-96f8-453e-8f72-f9032d5aa773
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnroll4 interface [Security],createRequestWStr method, IEnroll4.createRequestWStr, IEnroll4::createRequestWStr, XECR_CMC, XECR_PKCS10_V1_5, XECR_PKCS10_V2_0, XECR_PKCS7, createRequestWStr, createRequestWStr method [Security], createRequestWStr method [Security],IEnroll4 interface, security.ienroll4_createrequestwstr, xenroll/IEnroll4::createRequestWStr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.redist: 
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
 - IEnroll4.createRequestWStr
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll4::createRequestWStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createRequestWStr</b> method creates a PKCS #10, PKCS #7, or full <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Management over CMS</a> (CMC) format <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a> and stores it in a BLOB. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param Flags [in]

Value specifying the type of certificate request to create. Specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XECR_CMC"></a><a id="xecr_cmc"></a><dl>
<dt><b>XECR_CMC</b></dt>
</dl>
</td>
<td width="60%">
Full CMC

</td>
</tr>
<tr>
<td width="40%"><a id="XECR_PKCS10_V1_5"></a><a id="xecr_pkcs10_v1_5"></a><dl>
<dt><b>XECR_PKCS10_V1_5</b></dt>
</dl>
</td>
<td width="60%">
PKCS #10

</td>
</tr>
<tr>
<td width="40%"><a id="XECR_PKCS10_V2_0"></a><a id="xecr_pkcs10_v2_0"></a><dl>
<dt><b>XECR_PKCS10_V2_0</b></dt>
</dl>
</td>
<td width="60%">
PKCS #10 version 2

</td>
</tr>
<tr>
<td width="40%"><a id="XECR_PKCS7"></a><a id="xecr_pkcs7"></a><dl>
<dt><b>XECR_PKCS7</b></dt>
</dl>
</td>
<td width="60%">
PKCS #7

</td>
</tr>
</table>
 


### -param pwszDNName [in]

A pointer to a <b>null</b>-terminated Unicode string that contains the distinguished name (DN) of the entity for which the request is being made. The DN name must follow the <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.500</a> naming convention, for example "CN=User, O=Microsoft". If a two-letter prefix does not exist, an object identifier (OID) may be provided instead. This parameter may be <b>NULL</b>.


### -param pwszUsage [in]

A pointer to a <b>null</b>-terminated Unicode string that contains the OID that describes the purpose of the certificate being generated, for example, individual or commercial Authenticode certificate, or client authentication. You can also specify multiple OIDs separated by a comma.


### -param pblobRequest [out]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that receives the request.

When you have finished using this memory, free it by passing the <b>pbData</b> member of this structure to the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

