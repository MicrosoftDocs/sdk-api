---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWMDMOperation::GetObjectTotalSize


## -description



Windows Media Device Manager calls <b>GetObjectTotalSize</b> before a file is written to the device in order to retrieve the total size of the object, in bytes.




## -parameters




### -param pdwSize [out]

Pointer to a <b>DWORD</b> that, on return, specifies the low-order bits of the object size in bytes.


### -param pdwSizeHigh [out]

Pointer to a <b>DWORD</b> that, on return, specifies the high-order bits of the object size in bytes.


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



This method is called after the <a href="https://msdn.microsoft.com/4e1f4300-057d-40df-8e5c-75765f9ce337">GetObjectAttributes</a> method has been called. When transferring, the object implementing this interface is passed the total size of the content being sent.


#### Examples

The following C++ code implements GetObjectTotalSize. It uses the Win32 function GetFileInformationByHandle to retrieve the file size of the file about to be written to the device (m_File), and returns the values.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// About to start writing to the device.
HRESULT GetObjectTotalSize(DWORD*  pdwSize,    DWORD*  pdwSizeHigh)
{
    BY_HANDLE_FILE_INFORMATION fileInfo;
    GetFileInformationByHandle(
        m_File,
        &amp;fileInfo);

    *pdwSize = fileInfo.nFileSizeLow;
    *pdwSizeHigh = fileInfo.nFileSizeHigh;
    // TODO: Display the message: "IWMDMOperation event--GetObjectTotalSize."
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ff94191b-a0f2-4118-996c-d040f214fb9b">Handling File Transfers Manually</a>



<a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation Interface</a>



<a href="https://msdn.microsoft.com/009716e8-6a4e-4373-9a7c-69dad815e743">SetObjectTotalSize</a>
 

 

