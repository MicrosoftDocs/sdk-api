---
UID: NF:mswmdm.IWMDMStorage.SetAttributes
title: IWMDMStorage::SetAttributes (mswmdm.h)
description: The SetAttributes method sets the attributes of the storage.
helpviewer_keywords: ["IWMDMStorage interface [windows Media Device Manager]","SetAttributes method","IWMDMStorage.SetAttributes","IWMDMStorage::SetAttributes","IWMDMStorageSetAttributes","SetAttributes","SetAttributes method [windows Media Device Manager]","SetAttributes method [windows Media Device Manager]","IWMDMStorage interface","mswmdm/IWMDMStorage::SetAttributes","wmdm.iwmdmstorage_setattributes"]
old-location: wmdm\iwmdmstorage_setattributes.htm
tech.root: WMDM
ms.assetid: 7484e29a-5faf-4a11-9fc1-75aa5c9d72ef
ms.date: 12/05/2018
ms.keywords: IWMDMStorage interface [windows Media Device Manager],SetAttributes method, IWMDMStorage.SetAttributes, IWMDMStorage::SetAttributes, IWMDMStorageSetAttributes, SetAttributes, SetAttributes method [windows Media Device Manager], SetAttributes method [windows Media Device Manager],IWMDMStorage interface, mswmdm/IWMDMStorage::SetAttributes, wmdm.iwmdmstorage_setattributes
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
 - IWMDMStorage::SetAttributes
 - mswmdm/IWMDMStorage::SetAttributes
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
 - IWMDMStorage.SetAttributes
---

# IWMDMStorage::SetAttributes


## -description

The <b>SetAttributes</b> method sets the attributes of the storage.

## -parameters

### -param dwAttributes [in]

<b>DWORD</b> specifying the attributes to be set. The following table lists the attributes that can be set by this parameter.

<table>
<tr>
<th>Attribute
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_FILE_ATTR_AUDIO</td>
<td>This file contains audio data.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_DATA</td>
<td>This file contains non-audio data.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_CANPLAY</td>
<td>This audio file can be played by the device.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_CANDELETE</td>
<td>This file can be deleted.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_CANMOVE</td>
<td>This file or folder can be moved around on the storage medium.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_CANRENAME</td>
<td>This file or folder can be renamed.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_CANREAD</td>
<td>This file can be read by the host computer.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_MUSIC</td>
<td>This audio file contains music.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_AUDIOBOOK</td>
<td>This is an audio book file.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_HIDDEN</td>
<td>This file is hidden on the file system</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_SYSTEM</td>
<td>This is a system file</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_READONLY</td>
<td>This is a read-only file.</td>
</tr>
</table>

### -param pFormat [in]

Optional pointer to a <a href="/windows/desktop/WMDM/-waveformatex">_WAVEFORMATEX</a> structure that specifies audio information about the object.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Many of the attributes listed for <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes">GetAttributes</a> cannot be set, and so are not listed in the attribute table for <b>SetAttributes</b>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes">IWMDMStorage::GetAttributes</a>