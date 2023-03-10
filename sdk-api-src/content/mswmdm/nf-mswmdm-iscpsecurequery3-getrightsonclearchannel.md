---
UID: NF:mswmdm.ISCPSecureQuery3.GetRightsOnClearChannel
title: ISCPSecureQuery3::GetRightsOnClearChannel (mswmdm.h)
description: The GetRightsOnClearChannel method retrieves rights information for the current piece of content on a clear channel.
helpviewer_keywords: ["GetRightsOnClearChannel","GetRightsOnClearChannel method [windows Media Device Manager]","GetRightsOnClearChannel method [windows Media Device Manager]","ISCPSecureQuery3 interface","ISCPSecureQuery3 interface [windows Media Device Manager]","GetRightsOnClearChannel method","ISCPSecureQuery3.GetRightsOnClearChannel","ISCPSecureQuery3::GetRightsOnClearChannel","ISCPSecureQuery3GetRightsOnClearChannel","mswmdm/ISCPSecureQuery3::GetRightsOnClearChannel","wmdm.iscpsecurequery3_getrightsonclearchannel"]
old-location: wmdm\iscpsecurequery3_getrightsonclearchannel.htm
tech.root: WMDM
ms.assetid: ab64b790-848a-4c7f-9bf9-4a9b40bcc9cb
ms.date: 12/05/2018
ms.keywords: GetRightsOnClearChannel, GetRightsOnClearChannel method [windows Media Device Manager], GetRightsOnClearChannel method [windows Media Device Manager],ISCPSecureQuery3 interface, ISCPSecureQuery3 interface [windows Media Device Manager],GetRightsOnClearChannel method, ISCPSecureQuery3.GetRightsOnClearChannel, ISCPSecureQuery3::GetRightsOnClearChannel, ISCPSecureQuery3GetRightsOnClearChannel, mswmdm/ISCPSecureQuery3::GetRightsOnClearChannel, wmdm.iscpsecurequery3_getrightsonclearchannel
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
 - ISCPSecureQuery3::GetRightsOnClearChannel
 - mswmdm/ISCPSecureQuery3::GetRightsOnClearChannel
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
 - ISCPSecureQuery3.GetRightsOnClearChannel
---

# ISCPSecureQuery3::GetRightsOnClearChannel


## -description

The <b>GetRightsOnClearChannel</b> method retrieves rights information for the current piece of content on a clear channel.

## -parameters

### -param pData [in]

Pointer to data object.

### -param dwSize [in]

Number of bytes of data in the <i>pData</i> buffer.

### -param pbSPSessionKey [in]

Pointer to an array of bytes containing the session key for securing communication with the service provider to which <i>pStgGlobals</i> points.

### -param dwSessionKeyLen [in]

Length of the byte array to which <i>pbSPSessionKey</i> points.

### -param pStgGlobals [in]

Pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals</a> interface on the root storage of the media or device to or from which the file is being transferred.

### -param pProgressCallback [in]

Pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3">IWMDMProgress3</a> interface.

### -param ppRights [out]

Pointer to an array of <a href="/windows/desktop/WMDM/wmdmrights">WMDMRIGHTS</a> structures containing the rights information for this object. The array is allocated by this method and must be freed using <b>CoTaskMemFree</b>.

### -param pnRightsCount [out]

Number of <b>WMDMRIGHTS</b> structures in the <i>ppRights</i> array.

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
This method was called out of sequence. <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecurequery-getdatademands">ISCPSecureQuery::GetDataDemands</a> and then <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecurequery-examinedata">ISCPSecureQuery::ExamineData</a> must be called, in that order.

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
<dt><b>WMDM_E_NORIGHTS</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have the rights required to perform the requested operation.

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

This method is identical to <b>ISCPSecureQuery::GetRights</b> except that the parameters passed to this method are not encrypted. Consequently this method is more efficient.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3">ISCPSecureQuery3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecurequery-getrights">ISCPSecureQuery::GetRights</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals Interface</a>



<a href="/windows/desktop/WMDM/wmdmrights">WMDMRIGHTS</a>