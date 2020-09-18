---
UID: NF:mswmdm.IWMDMStorageControl.Read
title: IWMDMStorageControl::Read (mswmdm.h)
description: The Read method copies the current storage to the computer.
helpviewer_keywords: ["IWMDMStorageControl interface [windows Media Device Manager]","Read method","IWMDMStorageControl.Read","IWMDMStorageControl::Read","IWMDMStorageControlRead","Read","Read method [windows Media Device Manager]","Read method [windows Media Device Manager]","IWMDMStorageControl interface","mswmdm/IWMDMStorageControl::Read","wmdm.iwmdmstoragecontrol_read"]
old-location: wmdm\iwmdmstoragecontrol_read.htm
tech.root: WMDM
ms.assetid: 4b102666-b54b-4b60-b2e9-68def384268e
ms.date: 12/05/2018
ms.keywords: IWMDMStorageControl interface [windows Media Device Manager],Read method, IWMDMStorageControl.Read, IWMDMStorageControl::Read, IWMDMStorageControlRead, Read, Read method [windows Media Device Manager], Read method [windows Media Device Manager],IWMDMStorageControl interface, mswmdm/IWMDMStorageControl::Read, wmdm.iwmdmstoragecontrol_read
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
 - IWMDMStorageControl::Read
 - mswmdm/IWMDMStorageControl::Read
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
 - IWMDMStorageControl.Read
---

# IWMDMStorageControl::Read


## -description

The <b>Read</b> method copies the current storage to the computer.

## -parameters

### -param fuMode [in]

Processing mode used for the <b>Read</b> operation. The following table lists the processing modes that can be specified in the <i>fuMode</i> parameter. You must specify exactly one of the first two modes, and exactly one of the last three (WMDM_CONTENT) modes. If both WMDM_MODE_BLOCK and WMDM_MODE_THREAD are specified, block mode is used.

<table>
<tr>
<th>Mode
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_MODE_BLOCK</td>
<td>The operation is performed using block mode processing. The call will not return until the operation is finished.</td>
</tr>
<tr>
<td>WMDM_MODE_THREAD</td>
<td>The operation is performed using thread mode processing. The call will return immediately, and the operation is performed in a background thread.</td>
</tr>
<tr>
<td>WMDM_CONTENT_FILE</td>
<td>The caller requests that Windows Media Device Manager read the file from the portable device into a file on the hard disk. The caller should indicate, in the <i>pwszFileName</i> parameter, the full path and name of the file.</td>
</tr>
<tr>
<td>WMDM_CONTENT_FOLDER</td>
<td>The caller requests that Windows Media Device Manager read the specified folder, the contents, of the folder and the contents of any subfolders from the portable device onto the hard disk. The caller should indicate the full path of the target directory on the hard disk in the <i>pwszFileName</i> parameter.This is not currently supported by any Microsoft-provided service providers.

</td>
</tr>
<tr>
<td>WMDM_CONTENT_OPERATIONINTERFACE</td>
<td>The application-implemented <b>IWMDMOperation</b> interface is being used to read data, instead of passing in a file name.</td>
</tr>
</table>

### -param pwszFile [in]

Pointer to a fully qualified file name on the computer to which the content from the portable device is copied. The file name should include an extension; the extension from the current storage on the device will not be used. If WMDM_CONTENT_OPERATIONINTERFACE is specified in <i>fuMode</i>, this parameter is ignored.

### -param pProgress [in]

Optional pointer to a <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress</a> interface that has been implemented by the application to track the progress of ongoing operations.

### -param pOperation [in]

Optional pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation</a> interface, an optional set of methods used to enhance the transfer of content from a media device. This parameter must be <b>NULL</b> if WMDM_CONTENT_FILE or WMDM_CONTENT_FOLDER is specified in <i>fuMode</i>.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method will automatically overwrite existing files specified by <i>pwszFilename</i>. It can succeed even if

If the WMDM_MODE_THREAD flag is specified, you should obtain completion status by calling either <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress2-end2">IWMDMProgress2::End2</a> or <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress3-end3">IWMDMProgress3::End3</a>. These methods will ensure that the operation is complete and will also return an HRESULT with success or failure information.

If an application uses WMDM_MODE_THREAD and passes a non-<b>null</b><i>pProgress</i> parameter, the application must ensure that the object to which <i>pProgress</i> belongs is not destroyed until the read operation completes, because Windows Media Device Manager will send progress notifications to this object. This object can be destroyed only after it receives an End notification. Failure to do this will result in access violations.

## -see-also

<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getstatus">IWMDMDevice::GetStatus</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert">IWMDMStorageControl::Insert</a>