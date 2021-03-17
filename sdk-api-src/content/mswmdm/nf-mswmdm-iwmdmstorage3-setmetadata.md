---
UID: NF:mswmdm.IWMDMStorage3.SetMetadata
title: IWMDMStorage3::SetMetadata (mswmdm.h)
description: The SetMetadata method sets metadata on the storage.
helpviewer_keywords: ["IWMDMStorage3 interface [windows Media Device Manager]","SetMetadata method","IWMDMStorage3.SetMetadata","IWMDMStorage3::SetMetadata","IWMDMStorage3SetMetadata","SetMetadata","SetMetadata method [windows Media Device Manager]","SetMetadata method [windows Media Device Manager]","IWMDMStorage3 interface","mswmdm/IWMDMStorage3::SetMetadata","wmdm.iwmdmstorage3_setmetadata"]
old-location: wmdm\iwmdmstorage3_setmetadata.htm
tech.root: WMDM
ms.assetid: f06eb965-af34-4247-b8a6-0ac1ee4e4839
ms.date: 12/05/2018
ms.keywords: IWMDMStorage3 interface [windows Media Device Manager],SetMetadata method, IWMDMStorage3.SetMetadata, IWMDMStorage3::SetMetadata, IWMDMStorage3SetMetadata, SetMetadata, SetMetadata method [windows Media Device Manager], SetMetadata method [windows Media Device Manager],IWMDMStorage3 interface, mswmdm/IWMDMStorage3::SetMetadata, wmdm.iwmdmstorage3_setmetadata
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
 - IWMDMStorage3::SetMetadata
 - mswmdm/IWMDMStorage3::SetMetadata
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
 - IWMDMStorage3.SetMetadata
---

# IWMDMStorage3::SetMetadata


## -description

The <b>SetMetadata</b> method sets metadata on the storage.

## -parameters

### -param pMetadata [in]

An <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData</a> pointer containing metadata to set on the object. To create this interface, call <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject">CreateEmptyMetadataObject</a>.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Existing properties in the storage with the same name are overwritten. All other existing properties are not modified or lost.

To set properties for a Windows Portable Devices (WPD) device, an application would create an <b>IPortableDeviceValues</b> object and set each property into this collection. Then, the application would serialize the collection to a binary large object (BLOB). Once the data is serialized, the application would add it to the <b>IWMDMMetaData</b> referenced by the <i>pMetadata</i> argument using the g_wszWPDPassthroughPropertyValues metadata constant.


#### Examples

The following C++ code adds a subtitle as metadata to a storage (pStorage3) using the <b>IWMDMMetaData</b> interface retrieved from the storage previously (not shown).


```cpp

// Set metadata values on a storage.
WCHAR* station = L"Mysubtitle";
UINT numBytes = (wcslen(station) + 1) * sizeof(WCHAR); // WCHAR string is 2 * length of characters long
                                                       // plus the terminating null character.
hr = pMetadata->AddItem(WMDM_TYPE_STRING, g_wszWMDMMediaStationName, (BYTE*)station, numBytes) ;
BREAK_HR(hr, "Added a metadata value to the interface in TestUpdateMetadata.", "Couldn't add a metadata value to the interface in TestUpdateMetadata.");

// Add the metadata to the storage.
hr = pStorage3->SetMetadata(pMetadata);
BREAK_HR(hr, "Set metadata on the storage in TestUpdateMetadata.", "Couldn't set metadata on the storage in TestUpdateMetadata: " << hex << hr << dec);

```

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3">IWMDMStorage3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata">IWMDMStorage3::GetMetadata</a>



<a href="/windows/desktop/WMDM/setting-metadata-on-a-file">Setting Metadata on a File</a>