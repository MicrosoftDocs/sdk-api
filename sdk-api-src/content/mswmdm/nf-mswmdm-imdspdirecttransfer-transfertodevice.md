---
UID: NF:mswmdm.IMDSPDirectTransfer.TransferToDevice
title: IMDSPDirectTransfer::TransferToDevice
author: windows-sdk-content
description: The TransferToDevice method is called by Windows Media Device Manager to delegate content transfer content to the service provider. The source can be specified either as a file or as an operation interface.
old-location: wmdm\imdspdirecttransfer_transfertodevice.htm
tech.root: WMDM
ms.assetid: 7a95a23d-751e-4101-a150-3a1e47a14a95
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMDSPDirectTransfer interface [windows Media Device Manager],TransferToDevice method, IMDSPDirectTransfer.TransferToDevice, IMDSPDirectTransfer::TransferToDevice, IMDSPDirectTransferTransferToDevice, TransferToDevice, TransferToDevice method [windows Media Device Manager], TransferToDevice method [windows Media Device Manager],IMDSPDirectTransfer interface, mswmdm/IMDSPDirectTransfer::TransferToDevice, wmdm.imdspdirecttransfer_transfertodevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPDirectTransfer::TransferToDevice


## -description



The <b>TransferToDevice</b> method is called by Windows Media Device Manager to delegate content transfer content to the service provider. The source can be specified either as a file or as an operation interface.




## -parameters




### -param pwszSourceFilePath

TBD


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


#### - pwszSourceFileName [in]

Source file name. The value contained in this parameter should be ignored if WMDM_CONTENT_OPERATIONINTERFACE is specified.


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




<a href="https://msdn.microsoft.com/b053158c-9a1e-4da4-a428-7edceeaaee1e">IMDSPDirectTransfer Interface</a>



<a href="https://msdn.microsoft.com/453dbf9e-4b71-4ceb-80e2-eaa0cf4cd29d">IMDSPObject::Close</a>



<a href="https://msdn.microsoft.com/9e54bcbd-4f14-49e0-8211-2f79f024c80a">IMDSPObject::Open</a>



<a href="https://msdn.microsoft.com/29f16be5-9304-4b09-86e8-3f9e0e591a41">IMDSPObject::Write</a>



<a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData Interface</a>



<a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation Interface</a>



<a href="https://msdn.microsoft.com/9af022a6-19b4-41b7-b951-0acad6aab4a2">IWMDMProgress Interface</a>



<a href="https://msdn.microsoft.com/b56edc7a-0764-449a-95b4-da759e99fadd">IWMDMStorageControl Interface</a>
 

 

