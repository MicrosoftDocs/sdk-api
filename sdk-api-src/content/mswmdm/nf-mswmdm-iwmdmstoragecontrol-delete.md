---
UID: NF:mswmdm.IWMDMStorageControl.Delete
title: IWMDMStorageControl::Delete (mswmdm.h)
description: The Delete method permanently deletes this storage.
helpviewer_keywords: ["Delete","Delete method [windows Media Device Manager]","Delete method [windows Media Device Manager]","IWMDMStorageControl interface","IWMDMStorageControl interface [windows Media Device Manager]","Delete method","IWMDMStorageControl.Delete","IWMDMStorageControl::Delete","IWMDMStorageControlDelete","mswmdm/IWMDMStorageControl::Delete","wmdm.iwmdmstoragecontrol_delete"]
old-location: wmdm\iwmdmstoragecontrol_delete.htm
tech.root: WMDM
ms.assetid: f2b044d2-6386-4c2e-a437-5ebddf827fb4
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [windows Media Device Manager], Delete method [windows Media Device Manager],IWMDMStorageControl interface, IWMDMStorageControl interface [windows Media Device Manager],Delete method, IWMDMStorageControl.Delete, IWMDMStorageControl::Delete, IWMDMStorageControlDelete, mswmdm/IWMDMStorageControl::Delete, wmdm.iwmdmstoragecontrol_delete
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
 - IWMDMStorageControl::Delete
 - mswmdm/IWMDMStorageControl::Delete
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
 - IWMDMStorageControl.Delete
---

# IWMDMStorageControl::Delete


## -description

The <b>Delete</b> method permanently deletes this storage.

## -parameters

### -param fuMode [in]

One or two of the following flags, combined with a bitwise <b>OR</b>. Specify exactly one of the first two modes; the third mode is optional.

<table>
<tr>
<th>Mode
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_MODE_BLOCK</td>
<td>The operation is performed using block mode (synchronous) processing. The call will not return until the operation is finished.</td>
</tr>
<tr>
<td>WMDM_MODE_THREAD</td>
<td>The operation is performed using thread mode (asynchronous) processing. The call will return immediately, and the operation is performed in a background thread.</td>
</tr>
<tr>
<td>WMDM_MODE_RECURSIVE</td>
<td>If the storage object is a folder, it and its contents, and all subfolders and their contents are deleted.</td>
</tr>
</table>
 

4

### -param pProgress [in]

Optional pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress</a> interface to be used by Windows Media Device Manager to report progress back to the application.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

If the WMDM_MODE_THREAD flag is specified, you should obtain completion status by calling either <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress2-end2">IWMDMProgress2::End2</a> or <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress3-end3">IWMDMProgress3::End3</a>. These methods will ensure that the operation is complete and will also return an HRESULT with success or failure information.

When the <b>Delete</b> operation is finished, all references to the deleted object become invalid. The application must release these interfaces and any other interfaces or resources associated with the object.

If an application uses WMDM_MODE_THREAD and passes a non-null <i>pProgress</i> parameter, the application must ensure that the object to which <i>pProgress</i> belongs is not destroyed until the delete operation completes, because Windows Media Device Manager will send progress notifications to this object. This object can be destroyed only after it receives an End notification. Failure to do this will result in access violations.

## -see-also

<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getstatus">IWMDMDevice::GetStatus</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getstatus">IWMDMStorageGlobals::GetStatus</a>