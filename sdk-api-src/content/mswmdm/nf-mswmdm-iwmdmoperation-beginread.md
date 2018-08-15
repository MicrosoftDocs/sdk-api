---
UID: NF:mswmdm.IWMDMOperation.BeginRead
title: IWMDMOperation::BeginRead
author: windows-sdk-content
description: The BeginRead method indicates that a &#0034;read from device&#0034; action is beginning. Windows Media Device Manager only calls this method if the application calls IWMDMStorageControl::Read and passes in this IWMDMOperation interface.
old-location: wmdm\iwmdmoperation_beginread.htm
old-project: WMDM
ms.assetid: e72caaac-8992-4f11-8020-0455b3d730ad
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: BeginRead, BeginRead method [windows Media Device Manager], BeginRead method [windows Media Device Manager],IWMDMOperation interface, IWMDMOperation interface [windows Media Device Manager],BeginRead method, IWMDMOperation.BeginRead, IWMDMOperation::BeginRead, IWMDMOperationBeginRead, mswmdm/IWMDMOperation::BeginRead, wmdm.iwmdmoperation_beginread
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MSVidCtlStateList
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
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMOperation::BeginRead


## -description



The <b>BeginRead</b> method indicates that a "read from device" action is beginning. Windows Media Device Manager only calls this method if the application calls <a href="https://msdn.microsoft.com/4b102666-b54b-4b60-b2e9-68def384268e">IWMDMStorageControl::Read</a> and passes in this <b>IWMDMOperation</b> interface.




## -parameters






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



This method is called just before the Windows Media Device Manager calls <a href="https://msdn.microsoft.com/ba3f29d9-88cd-4050-aa9f-f9317745a16b">IWMDMOperation::TransferObjectData</a>.


#### Examples

The following C++ code example implements the <b>BeginRead</b> method and outputs a message when a read-from-device action is beginning.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ff94191b-a0f2-4118-996c-d040f214fb9b">Handling File Transfers Manually</a>



<a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation Interface</a>



<a href="https://msdn.microsoft.com/1b35b026-1fc1-44e8-befc-211d3387bc92">IWMDMOperation::BeginWrite</a>
 

 

