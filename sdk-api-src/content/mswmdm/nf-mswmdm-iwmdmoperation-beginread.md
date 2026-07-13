---
UID: NF:mswmdm.IWMDMOperation.BeginRead
title: IWMDMOperation::BeginRead (mswmdm.h)
description: The BeginRead method indicates that a &quot;read from device&quot; action is beginning. Windows Media Device Manager only calls this method if the application calls IWMDMStorageControl::Read and passes in this IWMDMOperation interface.
helpviewer_keywords: ["BeginRead","BeginRead method [windows Media Device Manager]","BeginRead method [windows Media Device Manager]","IWMDMOperation interface","IWMDMOperation interface [windows Media Device Manager]","BeginRead method","IWMDMOperation.BeginRead","IWMDMOperation::BeginRead","IWMDMOperationBeginRead","mswmdm/IWMDMOperation::BeginRead","wmdm.iwmdmoperation_beginread"]
old-location: wmdm\iwmdmoperation_beginread.htm
tech.root: WMDM
ms.assetid: e72caaac-8992-4f11-8020-0455b3d730ad
ms.date: 12/05/2018
ms.keywords: BeginRead, BeginRead method [windows Media Device Manager], BeginRead method [windows Media Device Manager],IWMDMOperation interface, IWMDMOperation interface [windows Media Device Manager],BeginRead method, IWMDMOperation.BeginRead, IWMDMOperation::BeginRead, IWMDMOperationBeginRead, mswmdm/IWMDMOperation::BeginRead, wmdm.iwmdmoperation_beginread
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
 - IWMDMOperation::BeginRead
 - mswmdm/IWMDMOperation::BeginRead
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
 - IWMDMOperation.BeginRead
---

# IWMDMOperation::BeginRead


## -description

The <b>BeginRead</b> method indicates that a "read from device" action is beginning. Windows Media Device Manager only calls this method if the application calls <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read">IWMDMStorageControl::Read</a> and passes in this <b>IWMDMOperation</b> interface.



## -returns

The application should return one of the following <b>HRESULT</b> values.

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
The read operation should continue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_USER_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The read operation should be cancelled without finishing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred, and the read operation should be cancelled without finishing.

</td>
</tr>
</table>

## -remarks

This method is called just before the Windows Media Device Manager calls <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata">IWMDMOperation::TransferObjectData</a>.


#### Examples

The following C++ code example implements the <b>BeginRead</b> method and outputs a message when a read-from-device action is beginning.


```cpp

HRESULT BeginRead()
{
    // TODO: Display the message: "IWMDMOperation event--BeginRead."

    // If the global handle of the source file is uninitialized, fail.
    if (m_File == INVALID_HANDLE_VALUE)
        return E_FAIL;

    // Global status to let TransferObjectData know what kind of
    // operation is happening.
    m_OperationStatus = OPERATION_READ;
    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/WMDM/handling-file-transfers-manually">Handling File Transfers Manually</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite">IWMDMOperation::BeginWrite</a>
