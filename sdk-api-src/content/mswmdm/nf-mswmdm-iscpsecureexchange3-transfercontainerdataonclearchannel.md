---
UID: NF:mswmdm.ISCPSecureExchange3.TransferContainerDataOnClearChannel
title: ISCPSecureExchange3::TransferContainerDataOnClearChannel (mswmdm.h)
description: The TransferContainerDataOnClearChannel method transfers container file data to the content provider through the clear channel.
helpviewer_keywords: ["ISCPSecureExchange3 interface [windows Media Device Manager]","TransferContainerDataOnClearChannel method","ISCPSecureExchange3.TransferContainerDataOnClearChannel","ISCPSecureExchange3::TransferContainerDataOnClearChannel","ISCPSecureExchange3TransferContainerDataOnClearChannel","TransferContainerDataOnClearChannel","TransferContainerDataOnClearChannel method [windows Media Device Manager]","TransferContainerDataOnClearChannel method [windows Media Device Manager]","ISCPSecureExchange3 interface","WMDM_SCP_NO_MORE_CHANGES","WMDM_SCP_TRANSFER_OBJECTDATA","mswmdm/ISCPSecureExchange3::TransferContainerDataOnClearChannel","wmdm.iscpsecureexchange3__transfercontainerdataonclearchannel"]
old-location: wmdm\iscpsecureexchange3__transfercontainerdataonclearchannel.htm
tech.root: WMDM
ms.assetid: aac0fc79-4615-442f-8c08-06addf40c799
ms.date: 12/05/2018
ms.keywords: ISCPSecureExchange3 interface [windows Media Device Manager],TransferContainerDataOnClearChannel method, ISCPSecureExchange3.TransferContainerDataOnClearChannel, ISCPSecureExchange3::TransferContainerDataOnClearChannel, ISCPSecureExchange3TransferContainerDataOnClearChannel, TransferContainerDataOnClearChannel, TransferContainerDataOnClearChannel method [windows Media Device Manager], TransferContainerDataOnClearChannel method [windows Media Device Manager],ISCPSecureExchange3 interface, WMDM_SCP_NO_MORE_CHANGES, WMDM_SCP_TRANSFER_OBJECTDATA, mswmdm/ISCPSecureExchange3::TransferContainerDataOnClearChannel, wmdm.iscpsecureexchange3__transfercontainerdataonclearchannel
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
 - ISCPSecureExchange3::TransferContainerDataOnClearChannel
 - mswmdm/ISCPSecureExchange3::TransferContainerDataOnClearChannel
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
 - ISCPSecureExchange3.TransferContainerDataOnClearChannel
---

# ISCPSecureExchange3::TransferContainerDataOnClearChannel


## -description

The <b>TransferContainerDataOnClearChannel</b> method transfers container file data to the content provider through the clear channel. The content provider breaks down the container internally and reports which parts of the content are available as they are extracted from the container.

This method is identical to <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-transfercontainerdata">ISCPSecureExchange::TransferContainerData</a> except that the parameters passed to this method are not encrypted. Consequently this method is more efficient.

## -parameters

### -param pDevice

Pointer to a device object.

### -param pData

Pointer to a buffer holding the current data being transferred from the container file.

### -param dwSize

Contains the number of bytes in the buffer.

### -param pProgressCallback

Progress callback on which the content provider can report progress of any steps that it might need to carry out. The step will be identified by the <i>EventId</i> parameter of <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3">IWMDMProgress3</a> methods.

### -param pfuReadyFlags

Flag indicating which parts of the container file are ready to be read. This parameter is included in the output message authentication code. The following flags indicate what is ready.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WMDM_SCP_TRANSFER_OBJECTDATA"></a><a id="wmdm_scp_transfer_objectdata"></a><dl>
<dt><b>WMDM_SCP_TRANSFER_OBJECTDATA</b></dt>
</dl>
</td>
<td width="60%">
Data of the object is available by calling the <a href="/windows/desktop/WMDM/iscpsecureexchange3--getobjectdataonclearchannel">GetObjectDataOnClearChannel</a> method.

</td>
</tr>
<tr>
<td width="40%"><a id="WMDM_SCP_NO_MORE_CHANGES"></a><a id="wmdm_scp_no_more_changes"></a><dl>
<dt><b>WMDM_SCP_NO_MORE_CHANGES</b></dt>
</dl>
</td>
<td width="60%">
The content provider has determined that it requires no further processing and/or modification of the file being transferred. Windows Media Device Manager can directly transfer the remainder of the file to the device.

</td>
</tr>
</table>

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
The method failed. Terminate interaction with the content provider.

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

Windows Media Device Manager calls this method repeatedly, transferring data from the container file to the content provider. Windows Media Device Manager eventually calls this method with <i>dwSize</i> set to zero to indicate that it has no more data to transfer. As the content provider collects the data and extracts the various objects from it, it reports back to Windows Media Device Manager which objects, if any, are available after each call. If no objects are available, the content provider returns S_OK with the <i>pfuReadyFlags</i> parameter set to zero. When the content provider has determined that it requires no further processing and/or modification of the file being transferred, the flag WMDM_SCP_NO_MORE_CHANGES is returned. Windows Media Device Manager can then directly transfer the remainder of the file to the device.

Object data is transferred from the content provider by calling the <b>GetObjectDataOnClearChannel</b> method. Windows Media Device Manager calls <b>GetObjectDataOnClearChannel</b> repeatedly until it returns zero in the third parameter, <i>pdwsize</i>.

The <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-transfercomplete">ISCPSecureExchange::TransferComplete</a> (or <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercompletefordevice">TransferCompleteForDevice</a> if a session is active) method is called by Windows Media Device Manager to signal the end of a data transfer.

Windows Media Device Manager passes the application-provided progress callback to the content provider in the <i>pProgressCallback</i> parameter. The content provider can use this parameter to provide progress notification for any steps that it needs to carry out. The step itself is identified by <i>EventId</i>, which is the first parameter of the methods of <b>IWMDMProgress3</b>. A specific content provider implementation will define <i>EventId</i> values for applications to use.

This method is identical to <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-transfercontainerdata">ISCPSecureExchange::TransferContainerData</a> except that the parameters passed to this method are not encrypted. Consequently this method is more efficient.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3">ISCPSecureExchange3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-transfercontainerdata">ISCPSecureExchange::TransferContainerData</a>