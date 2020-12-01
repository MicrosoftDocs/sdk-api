---
UID: NF:mswmdm.ISCPSecureQuery2.MakeDecision2
title: ISCPSecureQuery2::MakeDecision2 (mswmdm.h)
description: The MakeDecision2 method determines whether the secure content provider is responsible for the content by examining data that Windows Media Device Manager passes to this method.
helpviewer_keywords: ["ISCPSecureQuery2 interface [windows Media Device Manager]","MakeDecision2 method","ISCPSecureQuery2.MakeDecision2","ISCPSecureQuery2::MakeDecision2","ISCPSecureQuery2MakeDecision2","MakeDecision2","MakeDecision2 method [windows Media Device Manager]","MakeDecision2 method [windows Media Device Manager]","ISCPSecureQuery2 interface","mswmdm/ISCPSecureQuery2::MakeDecision2","wmdm.iscpsecurequery2_makedecision2"]
old-location: wmdm\iscpsecurequery2_makedecision2.htm
tech.root: WMDM
ms.assetid: a3031585-7a56-49d9-ad4b-d2f9e687dd6b
ms.date: 12/05/2018
ms.keywords: ISCPSecureQuery2 interface [windows Media Device Manager],MakeDecision2 method, ISCPSecureQuery2.MakeDecision2, ISCPSecureQuery2::MakeDecision2, ISCPSecureQuery2MakeDecision2, MakeDecision2, MakeDecision2 method [windows Media Device Manager], MakeDecision2 method [windows Media Device Manager],ISCPSecureQuery2 interface, mswmdm/ISCPSecureQuery2::MakeDecision2, wmdm.iscpsecurequery2_makedecision2
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
 - ISCPSecureQuery2::MakeDecision2
 - mswmdm/ISCPSecureQuery2::MakeDecision2
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
 - ISCPSecureQuery2.MakeDecision2
---

# ISCPSecureQuery2::MakeDecision2


## -description

The <b>MakeDecision2</b> method determines whether the secure content provider is responsible for the content by examining data that Windows Media Device Manager passes to this method. This method provides two output parameters for error handling, a default location for updating revoked components, and a bit flag indicating which components have been revoked.

## -parameters

### -param fuFlags [in]

Flags describing the data offered to the secure content provider for making decisions. This parameter must be included in the input message authentication code. One or more of the following flags can be combined using a bitwise <b>OR</b>.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_SCP_DECIDE_DATA</td>
<td>The <i>pData</i> parameter points to the data to be examined.</td>
</tr>
<tr>
<td>WMDM_MODE_TRANSFER_PROTECTED</td>
<td>The output object data from the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange">ISCPSecureExchange</a> interface must be protected. If Windows Media Device Manager sets neither or both mode flags, Windows Media Digital Rights Manager decides whether the output object data from the <b>ISCPSecureExchange</b> interface must be protected or unprotected.</td>
</tr>
<tr>
<td>WMDM_MODE_TRANSFER_UNPROTECTED</td>
<td>The output object data from the <b>ISCPSecureExchange</b> interface must be unprotected. If Windows Media Device Manager sets neither or both mode flags, Windows Media Digital Rights Manager decides whether the output object data from the <b>ISCPSecureExchange</b> interface must be protected or unprotected.</td>
</tr>
</table>

### -param pData [in]

Pointer to a data object containing the data to be examined. This parameter must be included in the input message authentication code and must be encrypted.

### -param dwSize [in]

<b>DWORD</b> containing the size of the file data.

### -param dwAppSec [in]

<b>DWORD</b> that contains the length, in bytes, of the <b>dwAppSec</b> member of the <a href="/windows/desktop/WMDM/wmdmrights">WMDMRIGHTS</a> structure of the service provider and secure content provider to be examined. This parameter must be included in the input message authentication code.

### -param pbSPSessionKey [in]

Pointer to an array of bytes containing the session key for securing communication with the service provider to which <i>pStgGlobals</i> points. This parameter must be included in the input message authentication code and must be encrypted.

### -param dwSessionKeyLen [in]

<b>DWORD</b> containing the session key length.

### -param pStorageGlobals [in]

Pointer to the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals</a> interface on the root storage of the media or device to or from which the file is being transferred. This parameter must be included in the input message authentication code.

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

Pointer to a <b>DWORD</b> containing the revocation bit flag. The flag value will be either zero, or one or more of the following flag names combined by using a bitwise <b>OR</b>.

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
<td>The secure content provider has been revoked and needs to be updated before any DRM-protected content can be transferred.</td>
</tr>
</table>

### -param pqwFileSize [in, out]

Pointer to a <b>QWORD</b> containing the file size. The secure content provider is responsible for updating this value or setting it to zero if the size of the destination file cannot be determined at this point.

### -param pUnknown [in]

Pointer to an unknown interface from the application.

### -param ppExchange [out]

Pointer to an exchange object that receives the exchange interface.

### -param abMac [in, out]

Array of eight bytes containing the message authentication code for the parameter data of this method. (WMDM_MAC_LENGTH is defined as 8.)

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_REVOKED</b></dt>
</dl>
</td>
<td width="60%">
The application certificate that the secure content provider uses to talk to the DRM client has been revoked.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2">ISCPSecureQuery2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecurequery-makedecision">ISCPSecureQuery::MakeDecision</a>