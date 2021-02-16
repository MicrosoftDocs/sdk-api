---
UID: NF:mswmdm.ISCPSecureQuery.MakeDecision
title: ISCPSecureQuery::MakeDecision (mswmdm.h)
description: The MakeDecision method determines whether access to the content is allowed. If access is allowed, this method returns the interface that will be used to access the content.
helpviewer_keywords: ["ISCPSecureQuery interface [windows Media Device Manager]","MakeDecision method","ISCPSecureQuery.MakeDecision","ISCPSecureQuery::MakeDecision","ISCPSecureQueryMakeDecision","MakeDecision","MakeDecision method [windows Media Device Manager]","MakeDecision method [windows Media Device Manager]","ISCPSecureQuery interface","mswmdm/ISCPSecureQuery::MakeDecision","wmdm.iscpsecurequery_makedecision"]
old-location: wmdm\iscpsecurequery_makedecision.htm
tech.root: WMDM
ms.assetid: cbcc8999-d7e4-4b67-a5ba-dd850ff7a07a
ms.date: 12/05/2018
ms.keywords: ISCPSecureQuery interface [windows Media Device Manager],MakeDecision method, ISCPSecureQuery.MakeDecision, ISCPSecureQuery::MakeDecision, ISCPSecureQueryMakeDecision, MakeDecision, MakeDecision method [windows Media Device Manager], MakeDecision method [windows Media Device Manager],ISCPSecureQuery interface, mswmdm/ISCPSecureQuery::MakeDecision, wmdm.iscpsecurequery_makedecision
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
 - ISCPSecureQuery::MakeDecision
 - mswmdm/ISCPSecureQuery::MakeDecision
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
 - ISCPSecureQuery.MakeDecision
---

# ISCPSecureQuery::MakeDecision


## -description

The <b>MakeDecision</b> method determines whether access to the content is allowed. If access is allowed, this method returns the interface that will be used to access the content.

## -parameters

### -param fuFlags [in]

Flags describing the data offered to the secure content provider for making decisions. This parameter must be included in the input message authentication code. The following flags can be present.

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
<td>The output object data from the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange">ISCPSecureExchange</a> interface must be protected. If Windows Media Device Manager sets neither or both mode flags, DRM decides whether the output object data from the <b>ISCPSecureExchange</b> interface must be protected or unprotected.</td>
</tr>
<tr>
<td>WMDM_MODE_TRANSFER_UNPROTECTED</td>
<td>The output object data from the <b>ISCPSecureExchange</b> interface must be unprotected. If Windows Media Device Manager sets neither or both mode flags, DRM decides whether the output object data from the <b>ISCPSecureExchange</b> interface must be protected or unprotected.</td>
</tr>
</table>

### -param pData [in]

Pointer to a data object containing the data to be examined. This parameter must be included in the input message authentication code and must be encrypted.

### -param dwSize [in]

<b>DWORD</b> that contains the length, in bytes, of the data to be examined. This parameter must be included in the input message authentication code.

### -param dwAppSec [in]

<b>DWORD</b> that indicates the current level of security of Windows Media Device Manager. This is the smaller of the current security levels of the application and the target service provider. This parameter must be included in the input message authentication code.

### -param pbSPSessionKey [in]

Pointer to an array of bytes containing the session key for securing communication with the service provider to which <i>pStgGlobals</i> points. This parameter must be included in the input message authentication code and must be encrypted.

### -param dwSessionKeyLen [in]

Length of the byte array to which <i>pbSPSessionKey</i> points. This parameter must be included in the input message authentication code.

### -param pStorageGlobals [in]

Pointer to the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals</a> interface on the root storage of the media or device to or from which the file is being transferred. This parameter must be included in the input message authentication code.

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

This method is called after the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecurequery-examinedata">ISCPSecureQuery::ExamineData</a> method, and makes the final decision whether access to the content is allowed.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange">ISCPSecureExchange Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecurequery2-makedecision2">ISCPSecureQuery2::MakeDecision2</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals Interface</a>