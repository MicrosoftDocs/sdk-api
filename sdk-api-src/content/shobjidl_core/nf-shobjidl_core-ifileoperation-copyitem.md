---
UID: NF:shobjidl_core.IFileOperation.CopyItem
title: IFileOperation::CopyItem
author: windows-sdk-content
description: Declares a single item that is to be copied to a specified destination.
old-location: shell\IFileOperation_CopyItem.htm
tech.root: shell
ms.assetid: 36d623b7-67c3-48b7-be9b-9264b5b8d919
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CopyItem, CopyItem method [Windows Shell], CopyItem method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],CopyItem method, IFileOperation.CopyItem, IFileOperation::CopyItem, _shell_IFileOperation_CopyItem, shell.IFileOperation_CopyItem, shobjidl_core/IFileOperation::CopyItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileOperation.CopyItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOperation::CopyItem


## -description


Declares a single item that is to be copied to a specified destination.


## -parameters




### -param psiItem [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the source item.


### -param psiDestinationFolder [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the destination folder to contain the copy of the item.


### -param pszCopyName [in]

Type: <b>LPCWSTR</b>

Pointer to a new name for the item after it has been copied. This is a null-terminated Unicode string and can be <b>NULL</b>. If <b>NULL</b>, the name of the destination item is the same as the source.


### -param pfopsItem [in]

Type: <b><a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a> object to be used for progress status and error notifications for this specific copy operation. If you call <a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">IFileOperation::Advise</a> for the overall operation, progress status and error notifications for the copy operation are included there, so set this parameter to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not copy the item, it merely declares the item to be copied. To copy an object, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::CopyItem</b> to declare the source item, destination folder, and destination name.</li>
<li>Call <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> to begin the copy operation.</li>
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




<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>



<a href="https://msdn.microsoft.com/9899cac2-bc10-422c-ab7f-2b8c1b893fc9">IFileOperation::CopyItems</a>



<a href="https://msdn.microsoft.com/2e5568a8-e689-48ca-82a1-36292d91a65b">PostCopyItem</a>



<a href="https://msdn.microsoft.com/ee436179-197d-49f6-986c-62a1ea930af5">PreCopyItem</a>
 

 

