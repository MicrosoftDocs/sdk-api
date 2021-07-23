---
UID: NF:shobjidl_core.IFileOperation.CopyItem
title: IFileOperation::CopyItem (shobjidl_core.h)
description: Declares a single item that is to be copied to a specified destination.
helpviewer_keywords: ["CopyItem","CopyItem method [Windows Shell]","CopyItem method [Windows Shell]","IFileOperation interface","IFileOperation interface [Windows Shell]","CopyItem method","IFileOperation.CopyItem","IFileOperation::CopyItem","_shell_IFileOperation_CopyItem","shell.IFileOperation_CopyItem","shobjidl_core/IFileOperation::CopyItem"]
old-location: shell\IFileOperation_CopyItem.htm
tech.root: shell
ms.assetid: 36d623b7-67c3-48b7-be9b-9264b5b8d919
ms.date: 12/05/2018
ms.keywords: CopyItem, CopyItem method [Windows Shell], CopyItem method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],CopyItem method, IFileOperation.CopyItem, IFileOperation::CopyItem, _shell_IFileOperation_CopyItem, shell.IFileOperation_CopyItem, shobjidl_core/IFileOperation::CopyItem
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileOperation::CopyItem
 - shobjidl_core/IFileOperation::CopyItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileOperation.CopyItem
---

# IFileOperation::CopyItem


## -description

Declares a single item that is to be copied to a specified destination.

## -parameters

### -param psiItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the source item.

### -param psiDestinationFolder [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the destination folder to contain the copy of the item.

### -param pszCopyName [in]

Type: <b>LPCWSTR</b>

Pointer to a new name for the item after it has been copied. This is a null-terminated Unicode string and can be <b>NULL</b>. If <b>NULL</b>, the name of the destination item is the same as the source.

### -param pfopsItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a> object to be used for progress status and error notifications for this specific copy operation. If you call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-advise">IFileOperation::Advise</a> for the overall operation, progress status and error notifications for the copy operation are included there, so set this parameter to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method does not copy the item, it merely declares the item to be copied. To copy an object, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::CopyItem</b> to declare the source item, destination folder, and destination name.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> to begin the copy operation.</li>
</ol>

#### Examples

The following example code shows a sample implementation of this method.


```cpp
HRESULT CopyItem(__in PCWSTR pszSrcItem, __in PCWSTR pszDest, PCWSTR pszNewName)
{
    //
    // Initialize COM as STA.
    //
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE); 
    if (SUCCEEDED(hr))
    {
        IFileOperation *pfo;
  
        //
        // Create the IFileOperation interface 
        //
        hr = CoCreateInstance(CLSID_FileOperation, 
                              NULL, 
                              CLSCTX_ALL, 
                              IID_PPV_ARGS(&pfo));
        if (SUCCEEDED(hr))
        {
            //
            // Set the operation flags. Turn off all UI from being shown to the
            // user during the operation. This includes error, confirmation,
            // and progress dialogs.
            //
            hr = pfo->SetOperationFlags(FOF_NO_UI);
            if (SUCCEEDED(hr))
            {
                //
                // Create an IShellItem from the supplied source path.
                //
                IShellItem *psiFrom = NULL;
                hr = SHCreateItemFromParsingName(pszSrcItem, 
                                                 NULL, 
                                                 IID_PPV_ARGS(&psiFrom));
                if (SUCCEEDED(hr))
                {
                    IShellItem *psiTo = NULL;
  
                    if (NULL != pszDest)
                    {
                        //
                        // Create an IShellItem from the supplied 
                        // destination path.
                        //
                        hr = SHCreateItemFromParsingName(pszDest, 
                                                         NULL, 
                                                         IID_PPV_ARGS(&psiTo));
                    }
                    
                    if (SUCCEEDED(hr))
                    {
                        //
                        // Add the operation
                        //
                        hr = pfo->CopyItem(psiFrom, psiTo, pszNewName, NULL);

                        if (NULL != psiTo)
                        {
                            psiTo->Release();
                        }
                    }
                    
                    psiFrom->Release();
                }
                
                if (SUCCEEDED(hr))
                {
                    //
                    // Perform the operation to copy the file.
                    //
                    hr = pfo->PerformOperations();
                }        
            }
            
            //
            // Release the IFileOperation interface.
            //
            pfo->Release();
        }
  
        CoUninitialize();
    }
    return hr;
}
```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-copyitems">IFileOperation::CopyItems</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperationprogresssink-postcopyitem">PostCopyItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperationprogresssink-precopyitem">PreCopyItem</a>