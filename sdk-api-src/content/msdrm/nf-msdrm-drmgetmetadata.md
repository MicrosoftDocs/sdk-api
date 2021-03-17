---
UID: NF:msdrm.DRMGetMetaData
title: DRMGetMetaData function (msdrm.h)
description: Retrieves metadata from an issuance license.
helpviewer_keywords: ["DRMGetMetaData","DRMGetMetaData function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetMetaData","rm.drmgetmetadata"]
old-location: rm\drmgetmetadata.htm
tech.root: rm
ms.assetid: bea3120a-11a2-42e9-bf1b-368cad25ede5
ms.date: 12/05/2018
ms.keywords: DRMGetMetaData, DRMGetMetaData function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetMetaData, rm.drmgetmetadata
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
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
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - DRMGetMetaData
 - msdrm/DRMGetMetaData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMGetMetaData
---

# DRMGetMetaData function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetMetaData</b> function retrieves metadata from an issuance license.

## -parameters

### -param hIssuanceLicense [in]

A handle to the issuance license to get the metadata from.

### -param puContentIdLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszContentId</i> buffer (required). This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszContentId</i> buffer.

### -param wszContentId [out, optional]

A pointer to a null-terminated Unicode string that receives the GUID that identifies the content. The size of this buffer is specified by the <i>puContentIdLength</i> parameter.

To determine the required size of  this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puContentIdLength</i> value.

### -param puContentIdTypeLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszContentIdType</i> buffer  (required). This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszContentIdType</i> buffer.

### -param wszContentIdType [out, optional]

A pointer to a null-terminated Unicode string that receives the type of GUID used to identify the content. The size of this buffer is specified by the <i>puContentIdTypeLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puContentIdTypeLength</i> value.

### -param puSKUIdLength [in, out, optional]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszSKUId</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszSKUId</i> buffer.

### -param wszSKUId [out, optional]

A pointer to a null-terminated Unicode string that receives the GUID that identifies the SKU of the content. The size of this buffer is specified by the <i>puSKUIdLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puSKUIdLength</i> value.

### -param puSKUIdTypeLength [in, out, optional]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszSKUIdType</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszSKUIdType</i> buffer.

### -param wszSKUIdType [out, optional]

A pointer to a null-terminated Unicode string that receives the type of SKU ID used to identify content. The size of this buffer is specified by the <i>puSKUIdTypeLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puSKUIdTypeLength</i> value.

### -param puContentTypeLength [in, out, optional]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszContentType</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszContentType</i> buffer.

### -param wszContentType [out, optional]

A pointer to a null-terminated Unicode string that receives the Multipurpose Internet Mail Extensions (MIME) type of the content. The size of this buffer is specified by the <i>puContentTypeLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puContentTypeLength</i> value.

### -param puContentNameLength [in, out, optional]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszContentName</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszContentName</i> buffer.

### -param wszContentName [out, optional]

A pointer to a null-terminated Unicode string that receives the name of the content. The size of this buffer is specified by the <i>puContentNameLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puContentNameLength</i> value.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetmetadata">DRMSetMetaData</a>