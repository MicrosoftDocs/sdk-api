---
UID: NF:mswmdm.ISCPSecureExchange.ObjectData
title: ISCPSecureExchange::ObjectData (mswmdm.h)
description: The ObjectData method transfers a block of object data back to Windows Media Device Manager.
helpviewer_keywords: ["ISCPSecureExchange interface [windows Media Device Manager]","ObjectData method","ISCPSecureExchange.ObjectData","ISCPSecureExchange::ObjectData","ISCPSecureExchangeObjectData","ObjectData","ObjectData method [windows Media Device Manager]","ObjectData method [windows Media Device Manager]","ISCPSecureExchange interface","mswmdm/ISCPSecureExchange::ObjectData","wmdm.iscpsecureexchange_objectdata"]
old-location: wmdm\iscpsecureexchange_objectdata.htm
tech.root: WMDM
ms.assetid: 825539e4-9162-40b7-bae0-336e728fb34e
ms.date: 12/05/2018
ms.keywords: ISCPSecureExchange interface [windows Media Device Manager],ObjectData method, ISCPSecureExchange.ObjectData, ISCPSecureExchange::ObjectData, ISCPSecureExchangeObjectData, ObjectData, ObjectData method [windows Media Device Manager], ObjectData method [windows Media Device Manager],ISCPSecureExchange interface, mswmdm/ISCPSecureExchange::ObjectData, wmdm.iscpsecureexchange_objectdata
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
 - ISCPSecureExchange::ObjectData
 - mswmdm/ISCPSecureExchange::ObjectData
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
 - ISCPSecureExchange.ObjectData
---

# ISCPSecureExchange::ObjectData


## -description

The <b>ObjectData</b> method transfers a block of object data back to Windows Media Device Manager.

## -parameters

### -param pData [out]

Pointer to a buffer to receive data. This parameter is included in the output message authentication code and is encrypted.

### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> containing the transfer size. This parameter must be included in both the input and output message authentication codes.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method failed. Terminate interaction with the secure content provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter is an invalid or <b>NULL</b> pointer.

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

To transfer data, Windows Media Device Manager calls the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-transfercontainerdata">TransferContainerData</a> method to obtain the container data. <b>ObjectData</b> is then called to transfer blocks of object data from the secure content provider to Windows Media Device Manager. If S_OK is returned with <i>pdwSize</i> set to zero, Windows Media Device Manager will request no further data.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange">ISCPSecureExchange Interface</a>