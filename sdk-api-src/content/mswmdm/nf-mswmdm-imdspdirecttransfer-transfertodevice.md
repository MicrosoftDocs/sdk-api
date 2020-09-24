---
UID: NF:mswmdm.IMDSPDirectTransfer.TransferToDevice
title: IMDSPDirectTransfer::TransferToDevice (mswmdm.h)
description: The TransferToDevice method is called by Windows Media Device Manager to delegate content transfer content to the service provider. The source can be specified either as a file or as an operation interface.
helpviewer_keywords: ["IMDSPDirectTransfer interface [windows Media Device Manager]","TransferToDevice method","IMDSPDirectTransfer.TransferToDevice","IMDSPDirectTransfer::TransferToDevice","IMDSPDirectTransferTransferToDevice","TransferToDevice","TransferToDevice method [windows Media Device Manager]","TransferToDevice method [windows Media Device Manager]","IMDSPDirectTransfer interface","mswmdm/IMDSPDirectTransfer::TransferToDevice","wmdm.imdspdirecttransfer_transfertodevice"]
old-location: wmdm\imdspdirecttransfer_transfertodevice.htm
tech.root: WMDM
ms.assetid: 7a95a23d-751e-4101-a150-3a1e47a14a95
ms.date: 12/05/2018
ms.keywords: IMDSPDirectTransfer interface [windows Media Device Manager],TransferToDevice method, IMDSPDirectTransfer.TransferToDevice, IMDSPDirectTransfer::TransferToDevice, IMDSPDirectTransferTransferToDevice, TransferToDevice, TransferToDevice method [windows Media Device Manager], TransferToDevice method [windows Media Device Manager],IMDSPDirectTransfer interface, mswmdm/IMDSPDirectTransfer::TransferToDevice, wmdm.imdspdirecttransfer_transfertodevice
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
 - IMDSPDirectTransfer::TransferToDevice
 - mswmdm/IMDSPDirectTransfer::TransferToDevice
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
 - IMDSPDirectTransfer.TransferToDevice
---

# IMDSPDirectTransfer::TransferToDevice


## -description

The <b>TransferToDevice</b> method is called by Windows Media Device Manager to delegate content transfer content to the service provider. The source can be specified either as a file or as an operation interface.

## -parameters

### -param pwszSourceFilePath [in]

Source file name. The value contained in this parameter should be ignored if WMDM_CONTENT_OPERATIONINTERFACE is specified.

### -param pSourceOperation [in]

Operation interface pointer that serves as the source. The value contained in this parameter should be ignored unless WMDM_CONTENT_OPERATIONINTERFACE is specified.

### -param fuFlags [in]

Flags that affect behavior of this method. The <i>fuFlags</i> parameter must be one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_CONTENT_FILE</td>
<td>The source is a file.</td>
</tr>
<tr>
<td>WMDM_CONTENT_FOLDER</td>
<td>The source is a folder.</td>
</tr>
<tr>
<td>WMDM_FILE_CREATE_OVERWRITE</td>
<td>Overwrite the destination file if it already exists.</td>
</tr>
</table>

### -param pwszDestinationName [in]

Content should be transferred to the device with this name. This parameter is required.

### -param pSourceMetaData [in]

Metadata interface pointer. The metadata object contains the source properties. This parameter is optional.

### -param pTransferProgress [in]

Progress callback interface. The service provider should update the information during the progress of the transfer. This parameter is optional.

### -param ppNewObject [out]

Newly created storage object. This parameter is optional. This can be <b>NULL</b> if the caller does not need to have the new object returned.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the following is true:

1) Both <i>pwszSourceFileName</i> and <i>pSourceOperation</i> are specified;

2) <i>pwszDestinationName</i> is not specified;

3) <i>fuFlags</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_DISK_FULL)</b></dt>
</dl>
</td>
<td width="60%">
There is not enough space on the disk.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_EXISTS)</b></dt>
</dl>
</td>
<td width="60%">
The file already exists and WMDM_FILE_CREATE_OVERWRITE was not specified. If the device allows duplicate file names, this could be acceptable and this error does not need to be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
Transfer of the specified content is not supported on the device.

</td>
</tr>
</table>

## -remarks

Windows Media Device Manager queries for <b>IMDSPDirectTransfer</b> interface during every transfer.

If the service provider supports the <b>IMDSPDirectTransfer</b> interface, Windows Media Device Manager simply delegates content transfer to the service provider. In this case, Windows Media Device Manager does not do any processing of the content before sending it to the service provider. The service provider gets full control of the source.

If the service provider does not support the <b>IMDSPDirectTransfer</b> interface, Windows Media Device Manager processes the source files and sends byte packets to the service provider. In addition, for protected content, Windows Media Device Manager calls the secure content provider to process the content before sending it to the service provider.

If <b>IMDSPDirectTransfer</b> is supported, Windows Media Device Manager delegates handling of the content to the service provider. This provides flexibility to the service provider for handling the content. In this case, the service provider is responsible for handling the protected content.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdirecttransfer">IMDSPDirectTransfer Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-close">IMDSPObject::Close</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-open">IMDSPObject::Open</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write">IMDSPObject::Write</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl Interface</a>