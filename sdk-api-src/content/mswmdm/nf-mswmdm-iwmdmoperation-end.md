---
UID: NF:mswmdm.IWMDMOperation.End
title: IWMDMOperation::End (mswmdm.h)
description: The End method indicates that a read or write operation is finished, whether successful or not, and it returns a completion code.
helpviewer_keywords: ["End","End method [windows Media Device Manager]","End method [windows Media Device Manager]","IWMDMOperation interface","IWMDMOperation interface [windows Media Device Manager]","End method","IWMDMOperation.End","IWMDMOperation::End","IWMDMOperationEnd","mswmdm/IWMDMOperation::End","wmdm.iwmdmoperation_end"]
old-location: wmdm\iwmdmoperation_end.htm
tech.root: WMDM
ms.assetid: f1a3f0b7-033d-4e93-aaca-43db88a9b705
ms.date: 12/05/2018
ms.keywords: End, End method [windows Media Device Manager], End method [windows Media Device Manager],IWMDMOperation interface, IWMDMOperation interface [windows Media Device Manager],End method, IWMDMOperation.End, IWMDMOperation::End, IWMDMOperationEnd, mswmdm/IWMDMOperation::End, wmdm.iwmdmoperation_end
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
 - IWMDMOperation::End
 - mswmdm/IWMDMOperation::End
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
 - IWMDMOperation.End
---

# IWMDMOperation::End


## -description

The <b>End</b> method indicates that a read or write operation is finished, whether successful or not, and it returns a completion code.

## -parameters

### -param phCompletionCode [in]

Completion code for the operation.

### -param pNewObject [in]

When sending to a device, a pointer to a new <b>IWMDMStorage</b> object representing the new object that has been sent to the device. When reading from a device, a pointer to the <b>IWMDMStorage</b> object that was read from the device.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The <b>End</b> method is called whether or not the transfer was successful, and is the last <b>IWMDMOperation</b> method called. This method can be used to signal the application to close all file handles and other objects required by the read or write operation.


#### Examples

The following C++ code closes a global file handle after a read or write action, and outputs a message.


```cpp

HRESULT End(HRESULT* phCompletionCode, IUnknown* pNewObject)
{
    // TODO: Display the message: "IWMDMOperation event--End."

    // Close the file handle now that we're done with it.
    if (m_File != INVALID_HANDLE_VALUE)
        if (!CloseHandle(m_File))
            // TODO: Display the message: "Couldn't close the file."

    // Reset global status flag.
    m_OperationStatus = OPERATION_UNINITIALIZED;
    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/WMDM/handling-file-transfers-manually">Handling File Transfers Manually</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation Interface</a>