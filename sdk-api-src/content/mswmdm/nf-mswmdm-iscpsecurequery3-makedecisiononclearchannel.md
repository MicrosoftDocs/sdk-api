---
UID: NF:mswmdm.ISCPSecureQuery3.MakeDecisionOnClearChannel
title: ISCPSecureQuery3::MakeDecisionOnClearChannel (mswmdm.h)
description: The MakeDecisionOnClearChannel method determines whether access to the content is allowed on a clear channel. If access is allowed, this method returns the interface used to access the content.
helpviewer_keywords: ["ISCPSecureQuery3 interface [windows Media Device Manager]","MakeDecisionOnClearChannel method","ISCPSecureQuery3.MakeDecisionOnClearChannel","ISCPSecureQuery3::MakeDecisionOnClearChannel","ISCPSecureQuery3MakeDecisionOnClearChannel","MakeDecisionOnClearChannel","MakeDecisionOnClearChannel method [windows Media Device Manager]","MakeDecisionOnClearChannel method [windows Media Device Manager]","ISCPSecureQuery3 interface","mswmdm/ISCPSecureQuery3::MakeDecisionOnClearChannel","wmdm.iscpsecurequery3_makedecisiononclearchannel"]
old-location: wmdm\iscpsecurequery3_makedecisiononclearchannel.htm
tech.root: WMDM
ms.assetid: 63ffa9ec-b8bb-4d5d-b380-e4dbe0fc865a
ms.date: 12/05/2018
ms.keywords: ISCPSecureQuery3 interface [windows Media Device Manager],MakeDecisionOnClearChannel method, ISCPSecureQuery3.MakeDecisionOnClearChannel, ISCPSecureQuery3::MakeDecisionOnClearChannel, ISCPSecureQuery3MakeDecisionOnClearChannel, MakeDecisionOnClearChannel, MakeDecisionOnClearChannel method [windows Media Device Manager], MakeDecisionOnClearChannel method [windows Media Device Manager],ISCPSecureQuery3 interface, mswmdm/ISCPSecureQuery3::MakeDecisionOnClearChannel, wmdm.iscpsecurequery3_makedecisiononclearchannel
req.header: mswmdm.h
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISCPSecureQuery3::MakeDecisionOnClearChannel
 - mswmdm/ISCPSecureQuery3::MakeDecisionOnClearChannel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - ISCPSecureQuery3.MakeDecisionOnClearChannel
---

# ISCPSecureQuery3::MakeDecisionOnClearChannel


## -description

The <b>MakeDecisionOnClearChannel</b> method determines whether access to the content is allowed on a clear channel. If access is allowed, this method returns the interface used to access the content.

## -parameters

### -param fuFlags [in]

Flags describing the data offered to the content provider for making decisions. The following flags can be present.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_SCP_DECIDE_DATA</td>
<td>The <i>pData</i> parameter points to data to be examined.</td>
</tr>
<tr>
<td>WMDM_MODE_TRANSFER_PROTECTED</td>
<td>The output object data from the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange">ISCPSecureExchange</a> interface must be protected. If Windows Media Device Manager sets neither or both mode flags, digital rights management (DRM) decides whether the output object data from the <b>ISCPSecureExchange</b> interface must be protected or unprotected.</td>
</tr>
<tr>
<td>WMDM_MODE_TRANSFER_UNPROTECTED</td>
<td>The output object data from the <b>ISCPSecureExchange</b> interface must be unprotected. If Windows Media Device Manager sets neither or both mode flags, digital rights management (DRM) decides whether the output object data from the <b>ISCPSecureExchange</b> interface must be protected or unprotected.</td>
</tr>
</table>

### -param pData [in]

Pointer to a data object containing the data to be examined.

### -param dwSize [in]

<b>DWORD</b> that contains the length, in bytes, of the data to be examined.

### -param dwAppSec [in]

<b>DWORD</b> that indicates the current level of security of Windows Media Device Manager. This is the smaller of the current security levels of the application and the target service provider.

### -param pbSPSessionKey [in]

Pointer to an array of bytes containing the session key for securing communication with the service provider to which <i>pStgGlobals</i> points.

### -param dwSessionKeyLen [in]

Length of the byte array to which <i>pbSPSessionKey</i> points.

### -param pStorageGlobals [in]

Pointer to the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals</a> interface on the root storage of the media or device to or from which the file is being transferred.

### -param pProgressCallback [in]

Pointer to a progress callback object.

### -param pAppCertApp [in]

Pointer to an application certificate of the application object.

### -param dwAppCertAppLen [in]

<b>DWORD</b> containing the length, in bytes, of the application certificate.

### -param pAppCertSP [in]

Pointer to the application certificate of the service provider object.

### -param dwAppCertSPLen [in]

<b>DWORD</b> containing the length, in bytes, of the application certificate.

### -param pszRevocationURL [in, out]

Pointer to a buffer to hold the revocation URL.

### -param pdwRevocationURLLen [in, out]

Pointer to a <b>DWORD</b> containing the size of the <i>rpszRevocationURL</i> buffer in bytes.

### -param pdwRevocationBitFlag [out]

Pointer to a <b>DWORD</b> containing the revocation bit flag. The flag value will be either zero or one or more of the following flag names combined by using a bitwise <b>OR</b>.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_WMDM_REVOKED</td>
<td>Windows Media Device Manager itself has been revoked.</td>
</tr>
<tr>
<td>WMDM_APP_REVOKED</td>
<td>The application has been revoked and needs to be updated before any DRM-protected content can be transferred.</td>
</tr>
<tr>
<td>WMDM_SP_REVOKED</td>
<td>The service provider has been revoked and needs to be updated before any DRM-protected content can be transferred to it.</td>
</tr>
<tr>
<td>WMDM_SCP_REVOKED</td>
<td>The content provider has been revoked and needs to be updated before any DRM-protected content can be transferred.</td>
</tr>
</table>

### -param pqwFileSize [in, out]

Pointer to a <b>QWORD</b> containing the file size. The content provider is responsible for updating this value or setting it to zero if the size of the destination file cannot be determined at this point.

### -param pUnknown [in]

Pointer to an unknown interface from the application.

### -param ppExchange [out]

Pointer to an exchange object that receives the exchange interface.

## -returns

If the method succeeds, it returns S_OK. If the method fails, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_CALL_OUT_OF_SEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
This method was called out of sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_MAC_CHECK_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The message authentication code is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_MOREDATA</b></dt>
</dl>
</td>
<td width="60%">
Windows Media Device Manager must call this method again with another packet of data. The size of the packet is determined by the <i>pdwMinDecisionData</i> parameter in the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecurequery-getdatademands">ISCPSecureQuery::GetDataDemands</a> method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have the rights required to perform the requested transfer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter is invalid or is a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

This method is identical to <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecurequery2-makedecision2">ISCPSecureQuery2::MakeDecision2</a> except that the parameters passed to this method are not encrypted. Consequently this method is more efficient.

## -see-also

<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecurequery2-makedecision2">ISCPSecureQuery2::MakeDecision2</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3">ISCPSecureQuery3 Interface</a>