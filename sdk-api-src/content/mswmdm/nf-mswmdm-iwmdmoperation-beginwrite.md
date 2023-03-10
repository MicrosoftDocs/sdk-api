---
UID: NF:mswmdm.IWMDMOperation.BeginWrite
title: IWMDMOperation::BeginWrite (mswmdm.h)
description: The BeginWrite method indicates that a &quot;write to device&quot; action is beginning. Windows Media Device Manager only calls this method if the application calls IWMDMStorageControl/2/3::Insert/2/3 and passes in this interface.
helpviewer_keywords: ["BeginWrite","BeginWrite method [windows Media Device Manager]","BeginWrite method [windows Media Device Manager]","IWMDMOperation interface","IWMDMOperation interface [windows Media Device Manager]","BeginWrite method","IWMDMOperation.BeginWrite","IWMDMOperation::BeginWrite","IWMDMOperationBeginWrite","mswmdm/IWMDMOperation::BeginWrite","wmdm.iwmdmoperation_beginwrite"]
old-location: wmdm\iwmdmoperation_beginwrite.htm
tech.root: WMDM
ms.assetid: 1b35b026-1fc1-44e8-befc-211d3387bc92
ms.date: 12/05/2018
ms.keywords: BeginWrite, BeginWrite method [windows Media Device Manager], BeginWrite method [windows Media Device Manager],IWMDMOperation interface, IWMDMOperation interface [windows Media Device Manager],BeginWrite method, IWMDMOperation.BeginWrite, IWMDMOperation::BeginWrite, IWMDMOperationBeginWrite, mswmdm/IWMDMOperation::BeginWrite, wmdm.iwmdmoperation_beginwrite
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
 - IWMDMOperation::BeginWrite
 - mswmdm/IWMDMOperation::BeginWrite
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
 - IWMDMOperation.BeginWrite
---

# IWMDMOperation::BeginWrite


## -description

The <b>BeginWrite</b> method indicates that a "write to device" action is beginning. Windows Media Device Manager only calls this method if the application calls <b>IWMDMStorageControl/2/3::Insert/2/3</b> and passes in this interface.



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

This method is called just before the Windows Media Device Manager calls <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata">IWMDMOperation::TransferObjectData</a> to begin writing data to the device.


#### Examples

The following C++ code example implements the <b>BeginWrite</b> method and outputs a message when a write-to-device action is beginning.


```cpp

HRESULT BeginWrite()
{
    // TODO: Display the message: "IWMDMOperation event--BeginWrite."
    
    // If the global handle of the destination file is uninitialized, fail.
    if (m_File == INVALID_HANDLE_VALUE)
        return E_FAIL;

    // Global status to let TransferObjectData know what kind of
    // operation is happening.
    m_OperationStatus = OPERATION_WRITE;
    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/WMDM/handling-file-transfers-manually">Handling File Transfers Manually</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread">IWMDMOperation::BeginRead</a>
