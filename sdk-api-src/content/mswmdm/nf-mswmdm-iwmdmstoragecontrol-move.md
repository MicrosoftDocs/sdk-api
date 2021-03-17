---
UID: NF:mswmdm.IWMDMStorageControl.Move
title: IWMDMStorageControl::Move (mswmdm.h)
description: The Move method moves the current storage to a new location on the device.
helpviewer_keywords: ["IWMDMStorageControl interface [windows Media Device Manager]","Move method","IWMDMStorageControl.Move","IWMDMStorageControl::Move","IWMDMStorageControlMove","Move","Move method [windows Media Device Manager]","Move method [windows Media Device Manager]","IWMDMStorageControl interface","mswmdm/IWMDMStorageControl::Move","wmdm.iwmdmstoragecontrol_move"]
old-location: wmdm\iwmdmstoragecontrol_move.htm
tech.root: WMDM
ms.assetid: 6a2cfca0-66e6-4358-99c1-161f7baccdd5
ms.date: 12/05/2018
ms.keywords: IWMDMStorageControl interface [windows Media Device Manager],Move method, IWMDMStorageControl.Move, IWMDMStorageControl::Move, IWMDMStorageControlMove, Move, Move method [windows Media Device Manager], Move method [windows Media Device Manager],IWMDMStorageControl interface, mswmdm/IWMDMStorageControl::Move, wmdm.iwmdmstoragecontrol_move
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
 - IWMDMStorageControl::Move
 - mswmdm/IWMDMStorageControl::Move
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
 - IWMDMStorageControl.Move
---

# IWMDMStorageControl::Move


## -description

The <b>Move</b> method moves the current storage to a new location on the device.

## -parameters

### -param fuMode [in]

Processing mode by which to invoke the <b>Move</b> operation and the type of move to make. Specify exactly one of the following two modes. If both modes are specified, block mode is used.

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
</table>
 

The following table lists flags that indicate where the object is moved to. One value from this table is combined with one value from the preceding Mode table using a bitwise <b>OR</b>.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_STORAGECONTROL_INSERTBEFORE</td>
<td>The object is inserted before the target object.</td>
</tr>
<tr>
<td>WMDM_STORAGECONTROL_INSERTINTO</td>
<td>The object is inserted into the target object.</td>
</tr>
<tr>
<td>WMDM_STORAGECONTROL_INSERTAFTER</td>
<td>The object is inserted after the target object.</td>
</tr>
</table>

### -param pTargetObject [in]

Pointer to the object before or after which you want to put the current object.

### -param pProgress [in]

Optional pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress</a> interface that has been implemented by the application to track the progress of an ongoing operation.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

A file or directory can be moved only within the same root storage.

If the WMDM_MODE_THREAD flag is specified, you should obtain completion status by calling either <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress2-end2">IWMDMProgress2::End2</a> or <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress3-end3">IWMDMProgress3::End3</a>. These methods will ensure that the operation is complete and will also return an HRESULT with success or failure information.

If an application uses WMDM_MODE_THREAD and passes a non-null <i>pProgress</i> parameter, the application must ensure that the object to which <i>pProgress</i> belongs is not destroyed until the move operation completes, because Windows Media Device Manager will send progress notifications to this object. This object can be destroyed only after it receives an End notification. Failure to do this will result in access violations.

## -see-also

<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getstatus">IWMDMDevice::GetStatus</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress">IWMDMProgress Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl Interface</a>