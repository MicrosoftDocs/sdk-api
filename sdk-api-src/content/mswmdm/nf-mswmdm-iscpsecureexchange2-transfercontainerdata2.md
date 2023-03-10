---
UID: NF:mswmdm.ISCPSecureExchange2.TransferContainerData2
title: ISCPSecureExchange2::TransferContainerData2 (mswmdm.h)
description: The TransferContainerData2 method transfers container file data to the secure content provider.
helpviewer_keywords: ["ISCPSecureExchange2 interface [windows Media Device Manager]","TransferContainerData2 method","ISCPSecureExchange2.TransferContainerData2","ISCPSecureExchange2::TransferContainerData2","ISCPSecureExchange2TransferContainerData2","TransferContainerData2","TransferContainerData2 method [windows Media Device Manager]","TransferContainerData2 method [windows Media Device Manager]","ISCPSecureExchange2 interface","mswmdm/ISCPSecureExchange2::TransferContainerData2","wmdm.iscpsecureexchange2_transfercontainerdata2"]
old-location: wmdm\iscpsecureexchange2_transfercontainerdata2.htm
tech.root: WMDM
ms.assetid: 7e130da3-2bef-4ff0-870c-31ac4c3767e5
ms.date: 12/05/2018
ms.keywords: ISCPSecureExchange2 interface [windows Media Device Manager],TransferContainerData2 method, ISCPSecureExchange2.TransferContainerData2, ISCPSecureExchange2::TransferContainerData2, ISCPSecureExchange2TransferContainerData2, TransferContainerData2, TransferContainerData2 method [windows Media Device Manager], TransferContainerData2 method [windows Media Device Manager],ISCPSecureExchange2 interface, mswmdm/ISCPSecureExchange2::TransferContainerData2, wmdm.iscpsecureexchange2_transfercontainerdata2
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
 - ISCPSecureExchange2::TransferContainerData2
 - mswmdm/ISCPSecureExchange2::TransferContainerData2
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
 - ISCPSecureExchange2.TransferContainerData2
---

# ISCPSecureExchange2::TransferContainerData2


## -description

The <b>TransferContainerData2</b> method transfers container file data to the secure content provider. The secure content provider breaks down the container internally and reports which parts of the content are available as they are extracted from the container. This method extends <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-transfercontainerdata">ISCPSecureExchange::TransferContainerData</a> by accepting a progress callback on which the secure content provider can send progress notifications for any of the steps it needs to carry out.

## -parameters

### -param pData [in]

Pointer to a buffer holding the current data being transferred from the container file. This parameter must be included in the input message authentication code and must be encrypted.

### -param dwSize [in]

<b>DWORD</b> that contains the number of bytes in the buffer. This parameter must be included in the input message authentication code.

### -param pProgressCallback [in]

Progress callback on which the secure content provider can report progress of any steps that it might need to carry out. The step will be identified by the <i>EventId</i> parameter of <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3">IWMDMProgress3</a> methods.

### -param pfuReadyFlags [out]

Flag indicating which parts of the container file are ready to be read. This parameter is included in the output message authentication code. The following flags indicate what is ready.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_SCP_TRANSFER_OBJECTDATA</td>
<td>Data of the object is available by calling the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata">ObjectData</a> method.</td>
</tr>
<tr>
<td>WMDM_SCP_NO_MORE_CHANGES</td>
<td>The secure content provider has determined that it requires no further processing and/or modification of the file being transferred. Windows Media Device Manager can directly transfer the remainder of the file to the device.</td>
</tr>
</table>

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
<dt><b>WMDM_E_NOT_CERTIFIED</b></dt>
</dl>
</td>
<td width="60%">
The caller is not authorized to use this interface.

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

Windows Media Device Manager calls this method repeatedly, transferring data from the container file to the secure content provider. Windows Media Device Manager eventually calls this method with <i>dwSize</i> set to zero to indicate that it has no more data to transfer. As the secure content provider collects the data and extracts the various objects from it, it reports back to Windows Media Device Manager which objects, if any, are available after each call. If no objects are available, the secure content provider returns S_OK with the <i>pfuReadyFlags</i> parameter set to zero. When the secure content provider has determined that it requires no further processing and/or modification of the file being transferred, the flag WMDM_SCP_NO_MORE_CHANGES is returned. Windows Media Device Manager can then directly transfer the remainder of the file to the device.

Object data is transferred from the secure content provider by calling the <b>ObjectData</b> method. Windows Media Device Manager calls <b>ObjectData</b> repeatedly until it returns zero in the second parameter, <i>dwBytesWrite</i>.

The <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-transfercomplete">TransferComplete</a> method is called by Windows Media Device Manager to signal the end of a secure transfer of data.

Windows Media Device Manager passes the application-provided progress callback to the secure content provider in the <i>pProgressCallback</i> parameter. The secure content provider can use this parameter to provide progress notification for any steps that it needs to carry out. The step itself is identified by <i>EventId</i>, which is the first parameter of the methods of <b>IWMDMProgress3</b>. A specific secure content provider implementation will define <i>EventId</i> values for applications to use.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange">ISCPSecureExchange Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2">ISCPSecureExchange2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata">ISCPSecureExchange::ObjectData</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3">IWMDMProgress3 Interface</a>