---
UID: NF:mswmdm.IWMDMOperation.BeginWrite
title: IWMDMOperation::BeginWrite
author: windows-sdk-content
description: The BeginWrite method indicates that a &#0034;write to device&#0034; action is beginning. Windows Media Device Manager only calls this method if the application calls IWMDMStorageControl/2/3::Insert/2/3 and passes in this interface.
old-location: wmdm\iwmdmoperation_beginwrite.htm
old-project: WMDM
ms.assetid: 1b35b026-1fc1-44e8-befc-211d3387bc92
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: BeginWrite, BeginWrite method [windows Media Device Manager], BeginWrite method [windows Media Device Manager],IWMDMOperation interface, IWMDMOperation interface [windows Media Device Manager],BeginWrite method, IWMDMOperation.BeginWrite, IWMDMOperation::BeginWrite, IWMDMOperationBeginWrite, mswmdm/IWMDMOperation::BeginWrite, wmdm.iwmdmoperation_beginwrite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMOperation.BeginWrite
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMOperation::BeginWrite


## -description



The <b>BeginWrite</b> method indicates that a "write to device" action is beginning. Windows Media Device Manager only calls this method if the application calls <b>IWMDMStorageControl/2/3::Insert/2/3</b> and passes in this interface.




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



This method is called just before the Windows Media Device Manager calls <a href="https://msdn.microsoft.com/ba3f29d9-88cd-4050-aa9f-f9317745a16b">IWMDMOperation::TransferObjectData</a> to begin writing data to the device.


#### Examples

The following C++ code example implements the <b>BeginWrite</b> method and outputs a message when a write-to-device action is beginning.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ff94191b-a0f2-4118-996c-d040f214fb9b">Handling File Transfers Manually</a>



<a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation Interface</a>



<a href="https://msdn.microsoft.com/e72caaac-8992-4f11-8020-0455b3d730ad">IWMDMOperation::BeginRead</a>
 

 

