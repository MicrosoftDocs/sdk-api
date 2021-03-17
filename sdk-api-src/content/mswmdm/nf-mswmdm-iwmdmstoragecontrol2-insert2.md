---
UID: NF:mswmdm.IWMDMStorageControl2.Insert2
title: IWMDMStorageControl2::Insert2 (mswmdm.h)
description: The Insert2 method puts content into/next to the storage. This method extends IWMDMStorageControl::Insert by allowing the application to specify a new destination name, and provide a pointer to a custom COM object.
helpviewer_keywords: ["IWMDMStorageControl2 interface [windows Media Device Manager]","Insert2 method","IWMDMStorageControl2.Insert2","IWMDMStorageControl2::Insert2","IWMDMStorageControl2Insert2","Insert2","Insert2 method [windows Media Device Manager]","Insert2 method [windows Media Device Manager]","IWMDMStorageControl2 interface","mswmdm/IWMDMStorageControl2::Insert2","wmdm.iwmdmstoragecontrol2_insert2"]
old-location: wmdm\iwmdmstoragecontrol2_insert2.htm
tech.root: WMDM
ms.assetid: bc6cc03c-e13a-45d8-afcb-1fadd5f4dd8e
ms.date: 12/05/2018
ms.keywords: IWMDMStorageControl2 interface [windows Media Device Manager],Insert2 method, IWMDMStorageControl2.Insert2, IWMDMStorageControl2::Insert2, IWMDMStorageControl2Insert2, Insert2, Insert2 method [windows Media Device Manager], Insert2 method [windows Media Device Manager],IWMDMStorageControl2 interface, mswmdm/IWMDMStorageControl2::Insert2, wmdm.iwmdmstoragecontrol2_insert2
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
 - IWMDMStorageControl2::Insert2
 - mswmdm/IWMDMStorageControl2::Insert2
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
 - IWMDMStorageControl2.Insert2
---

# IWMDMStorageControl2::Insert2


## -description

The <b>Insert2</b> method puts content into/next to the storage. This method extends <b>IWMDMStorageControl::Insert</b> by allowing the application to specify a new destination name, and provide a pointer to a custom COM object.

## -parameters

### -param fuMode [in]

Processing mode used for the <b>Insert2</b> operation. The following table lists the processing modes that can be specified in the <b>fuMode</b> parameter. You must specify exactly one of the first two modes, exactly one of the STORAGECONTROL modes, and exactly one of the CONTENT modes. If both WMDM_MODE_BLOCK and WMDM_MODE_THREAD are specified, block mode is used.

<table>
<tr>
<th>Combinations
                </th>
<th>Mode
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Exactly one of:</td>
<td>WMDM_MODE_BLOCK</td>
<td>The operation is performed using block mode processing. The call will not return until the operation is finished.</td>
</tr>
<tr>
<td>-</td>
<td>WMDM_MODE_THREAD</td>
<td>The operation is performed using thread mode processing. The call will return immediately, and the operation is performed in a background thread.</td>
</tr>
<tr>
<td>Optional</td>
<td>WMDM_MODE_QUERY</td>
<td>A test is performed to determine whether the insert operation could succeed, but the insert will not be performed.</td>
</tr>
<tr>
<td>Exactly one of:</td>
<td>WMDM_STORAGECONTROL_INSERTBEFORE</td>
<td>The object is inserted before the target object.</td>
</tr>
<tr>
<td>-</td>
<td>WMDM_STORAGECONTROL_INSERTAFTER</td>
<td>The object is inserted after the target object.</td>
</tr>
<tr>
<td>-</td>
<td>WMDM_STORAGECONTROL_INSERTINTO</td>
<td>The object is inserted into the current object. This will only work if the current object is a folder.</td>
</tr>
<tr>
<td>Optional</td>
<td>WMDM_FILE_CREATE_OVERWRITE</td>
<td>The object will replace the target object.</td>
</tr>
<tr>
<td>Exactly one of:</td>
<td>WMDM_CONTENT_FILE</td>
<td>The content being inserted is a file.</td>
</tr>
<tr>
<td>-</td>
<td>WMDM_CONTENT_FOLDER</td>
<td>The content being inserted is a folder. This will not transfer the contents of the folder.</td>
</tr>
<tr>
<td>Optional</td>
<td>WMDM_CONTENT_OPERATIONINTERFACE</td>
<td>The content being inserted is an operation interface. The data for the content should be written to the application-implemented <b>IWMDMOperation</b> interface.</td>
</tr>
<tr>
<td>Optional</td>
<td>WMDM_MODE_PROGRESS</td>
<td>Progress notifications should be sent through the <i>pProgress</i> parameter.</td>
</tr>
<tr>
<td>Optional one of:</td>
<td>WMDM_MODE_TRANSFER_PROTECTED</td>
<td>The insertion is in protected transfer mode.</td>
</tr>
<tr>
<td>-</td>
<td>WMDM_MODE_TRANSFER_UNPROTECTED</td>
<td>The insertion is in unprotected transfer mode.</td>
</tr>
</table>

### -param pwszFileSource [in]

Pointer to a wide-character, <b>null</b>-terminated string indicating the full name and path of the object to send to the device. This parameter must be <b>NULL</b> if WMDM_CONTENT_OPERATIONINTERFACE is specified in <i>fuMode</i>.

### -param pwszFileDest [in]

Optional name of file on the device. If not specified and the application passes an <b>IWMDMOperation</b> pointer to <i>pOperation</i>, Windows Media Device Manager will request a destination name by calling <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectname">IWMDMOperation::GetObjectName</a>. If not specified and the application does not use <i>pOperation</i>, the original file name and extension are used (without the path).

### -param pOperation [in]

Optional pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation</a> interface, to control the transfer of content to a media device. If specified, <i>fuMode</i> must include the WMDM_CONTENT_OPERATIONINTERFACE flag. This parameter must be <b>NULL</b> if WMDM_CONTENT_FILE or WMDM_CONTENT_FOLDER is specified in <i>fuMode</i>.

### -param pProgress [in]

Optional pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress</a> interface to report action progress back to the application. If specified, <i>fuMode</i> should include WMDM_MODE_PROGRESS.

### -param pUnknown [in]

Optional <b>IUnknown</b> pointer of any custom COM object to be passed to the secure content provider. This makes it possible to pass custom information to a secure content provider if the application has sufficient information about the secure content provider.

### -param ppNewObject [out]

Pointer to an <b>IWMDMStorage</b> interface that will contain the new content. The caller must release this interface when finished with it.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

If the device supports <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3">IWMDMStorageControl3::Insert3</a>, that is the preferred method to use.

If the WMDM_MODE_THREAD flag is specified, you should obtain completion status by calling either <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress2-end2">IWMDMProgress2::End2</a> or <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress3-end3">IWMDMProgress3::End3</a>. These methods will ensure that the operation is complete and will also return an HRESULT with success or failure information.

If an application uses WMDM_MODE_THREAD and passes a non-<b>null</b><i>pProgress</i> parameter, the application must ensure that the object to which <i>pProgress</i> belongs is not destroyed until the insert operation completes, because Windows Media Device Manager will send progress notifications to this object. This object can be destroyed only after it receives an End notification. Failure to do this will result in access violations.

## -see-also

<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getstatus">IWMDMDevice::GetStatus</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol2">IWMDMStorageControl2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3">IWMDMStorageControl3::Insert3</a>