---
UID: NF:mswmdm.IWMDMOperation.GetObjectAttributes
title: IWMDMOperation::GetObjectAttributes (mswmdm.h)
description: The GetObjectAttributes method allows the application to specify attributes for an object being written to a device. Windows Media Device Manager calls this method before a file is written to the device in order to learn the file's attributes.
helpviewer_keywords: ["GetObjectAttributes","GetObjectAttributes method [windows Media Device Manager]","GetObjectAttributes method [windows Media Device Manager]","IWMDMOperation interface","IWMDMOperation interface [windows Media Device Manager]","GetObjectAttributes method","IWMDMOperation.GetObjectAttributes","IWMDMOperation::GetObjectAttributes","IWMDMOperationGetObjectAttributes","mswmdm/IWMDMOperation::GetObjectAttributes","wmdm.iwmdmoperation_getobjectattributes"]
old-location: wmdm\iwmdmoperation_getobjectattributes.htm
tech.root: WMDM
ms.assetid: 4e1f4300-057d-40df-8e5c-75765f9ce337
ms.date: 12/05/2018
ms.keywords: GetObjectAttributes, GetObjectAttributes method [windows Media Device Manager], GetObjectAttributes method [windows Media Device Manager],IWMDMOperation interface, IWMDMOperation interface [windows Media Device Manager],GetObjectAttributes method, IWMDMOperation.GetObjectAttributes, IWMDMOperation::GetObjectAttributes, IWMDMOperationGetObjectAttributes, mswmdm/IWMDMOperation::GetObjectAttributes, wmdm.iwmdmoperation_getobjectattributes
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
 - IWMDMOperation::GetObjectAttributes
 - mswmdm/IWMDMOperation::GetObjectAttributes
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
 - IWMDMOperation.GetObjectAttributes
---

# IWMDMOperation::GetObjectAttributes


## -description

The <b>GetObjectAttributes</b> method allows the application to specify attributes for an object being written to a device. Windows Media Device Manager calls this method before a file is written to the device in order to learn the file's attributes.

## -parameters

### -param pdwAttributes [out]

Pointer to a <b>DWORD</b> that specifies the attributes defined in the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes">IWMDMStorage::GetAttributes</a> method.

### -param pFormat [out]

Pointer to a <a href="/windows/desktop/WMDM/-waveformatex">_WAVEFORMATEX</a> structure that specifies the audio format for files with audio data attributes.

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

When transferring data to the device, you should provide object attributes for optimal transference.


#### Examples

The following C++ code implements the <b>GetObjectAttributes</b> method. It tries to determine if the file being read (m_File) is a file or folder, and set the returned attributes accordingly.


```cpp

HRESULT GetObjectAttributes(DWORD* pdwAttributes, _WAVEFORMATEX* pFormat)
{
    // TODO: Display the message: IWMDMOperation event--GetObjectAttributes.
    *pdwAttributes = WMDM_FILE_ATTR_FILE | 
        WMDM_STORAGE_ATTR_REMOVABLE | 
        WMDM_FILE_ATTR_AUDIO;

    BY_HANDLE_FILE_INFORMATION fileInformation;
    if (GetFileInformationByHandle(m_File, &fileInformation))
    {
        if (fileInformation.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY)
            *pdwAttributes |= WMDM_FILE_ATTR_FOLDER;
        else
            *pdwAttributes |= WMDM_FILE_ATTR_FILE;

        if (fileInformation.dwFileAttributes & FILE_ATTRIBUTE_READONLY)
            *pdwAttributes |= FILE_ATTRIBUTE_READONLY;
    }

    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/WMDM/handling-file-transfers-manually">Handling File Transfers Manually</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation">IWMDMOperation Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes">IWMDMOperation::SetObjectAttributes</a>