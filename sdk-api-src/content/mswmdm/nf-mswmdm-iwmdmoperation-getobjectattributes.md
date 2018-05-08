---
UID: NF:mswmdm.IWMDMOperation.GetObjectAttributes
title: IWMDMOperation::GetObjectAttributes
author: windows-driver-content
description: The GetObjectAttributes method allows the application to specify attributes for an object being written to a device. Windows Media Device Manager calls this method before a file is written to the device in order to learn the file's attributes.
old-location: wmdm\iwmdmoperation_getobjectattributes.htm
old-project: WMDM
ms.assetid: 4e1f4300-057d-40df-8e5c-75765f9ce337
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: GetObjectAttributes, GetObjectAttributes method [windows Media Device Manager], GetObjectAttributes method [windows Media Device Manager],IWMDMOperation interface, IWMDMOperation interface [windows Media Device Manager],GetObjectAttributes method, IWMDMOperation.GetObjectAttributes, IWMDMOperation::GetObjectAttributes, IWMDMOperationGetObjectAttributes, mswmdm/IWMDMOperation::GetObjectAttributes, wmdm.iwmdmoperation_getobjectattributes
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IWMDMOperation.GetObjectAttributes
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IWMDMOperation::GetObjectAttributes


## -description



The <b>GetObjectAttributes</b> method allows the application to specify attributes for an object being written to a device. Windows Media Device Manager calls this method before a file is written to the device in order to learn the file's attributes.




## -parameters




### -param pdwAttributes [out]

Pointer to a <b>DWORD</b> that specifies the attributes defined in the <a href="https://msdn.microsoft.com/e43139d2-260a-4f27-a06c-aca741204663">IWMDMStorage::GetAttributes</a> method.


### -param pFormat [out]

Pointer to a <a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a> structure that specifies the audio format for files with audio data attributes.


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



When transferring data to the device, you should provide object attributes for optimal transferrence.


#### Examples

The following C++ code implements the <b>GetObjectAttributes</b> method. It tries to determine if the file being read (m_File) is a file or folder, and set the returned attributes accordingly.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT GetObjectAttributes(DWORD* pdwAttributes, _WAVEFORMATEX* pFormat)
{
    // TODO: Display the message: IWMDMOperation event--GetObjectAttributes.
    *pdwAttributes = WMDM_FILE_ATTR_FILE | 
        WMDM_STORAGE_ATTR_REMOVABLE | 
        WMDM_FILE_ATTR_AUDIO;

    BY_HANDLE_FILE_INFORMATION fileInformation;
    if (GetFileInformationByHandle(m_File, &amp;fileInformation))
    {
        if (fileInformation.dwFileAttributes &amp; FILE_ATTRIBUTE_DIRECTORY)
            *pdwAttributes |= WMDM_FILE_ATTR_FOLDER;
        else
            *pdwAttributes |= WMDM_FILE_ATTR_FILE;

        if (fileInformation.dwFileAttributes &amp; FILE_ATTRIBUTE_READONLY)
            *pdwAttributes |= FILE_ATTRIBUTE_READONLY;
    }

    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ff94191b-a0f2-4118-996c-d040f214fb9b">Handling File Transfers Manually</a>



<a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation Interface</a>



<a href="https://msdn.microsoft.com/0ee2eabe-c20d-48fe-96f4-cb4143869462">IWMDMOperation::SetObjectAttributes</a>
 

 

