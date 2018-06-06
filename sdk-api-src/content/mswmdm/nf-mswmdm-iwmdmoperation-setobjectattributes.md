---
UID: NF:mswmdm.IWMDMOperation.SetObjectAttributes
title: IWMDMOperation::SetObjectAttributes
author: windows-sdk-content
description: The SetObjectAttributes method specifies the file attributes. This method is currently not called by Windows Media Device Manager.
old-location: wmdm\iwmdmoperation_setobjectattributes.htm
old-project: WMDM
ms.assetid: 0ee2eabe-c20d-48fe-96f4-cb4143869462
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWMDMOperation interface [windows Media Device Manager],SetObjectAttributes method, IWMDMOperation.SetObjectAttributes, IWMDMOperation::SetObjectAttributes, IWMDMOperationSetObjectAttributes, SetObjectAttributes, SetObjectAttributes method [windows Media Device Manager], SetObjectAttributes method [windows Media Device Manager],IWMDMOperation interface, mswmdm/IWMDMOperation::SetObjectAttributes, wmdm.iwmdmoperation_setobjectattributes
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMOperation.SetObjectAttributes
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMOperation::SetObjectAttributes


## -description



The <b>SetObjectAttributes</b> method specifies the file attributes. This method is currently not called by Windows Media Device Manager.




## -parameters




### -param dwAttributes [in]

<b>DWORD</b> specifying the object attributes as defined in the <a href="https://msdn.microsoft.com/7484e29a-5faf-4a11-9fc1-75aa5c9d72ef">IWMDMStorage::SetAttributes</a> method.


### -param pFormat [in]

Pointer to a <a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a> structure specifying the format for files with audio data attributes. If the file contains audio data, this parameter should be filled.


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



Audio attributes include the number of samples per second, the number of bytes per sample, and so on.




## -see-also




<a href="https://msdn.microsoft.com/ff94191b-a0f2-4118-996c-d040f214fb9b">Handling File Transfers Manually</a>



<a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation Interface</a>



<a href="https://msdn.microsoft.com/4e1f4300-057d-40df-8e5c-75765f9ce337">IWMDMOperation::GetObjectAttributes</a>
 

 

