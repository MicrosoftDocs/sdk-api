---
UID: NF:mswmdm.IWMDMStorageGlobals.GetCapabilities
title: IWMDMStorageGlobals::GetCapabilities (mswmdm.h)
description: The GetCapabilities method retrieves the capabilities of the root storage medium.
helpviewer_keywords: ["GetCapabilities","GetCapabilities method [windows Media Device Manager]","GetCapabilities method [windows Media Device Manager]","IWMDMStorageGlobals interface","IWMDMStorageGlobals interface [windows Media Device Manager]","GetCapabilities method","IWMDMStorageGlobals.GetCapabilities","IWMDMStorageGlobals::GetCapabilities","IWMDMStorageGlobalsGetCapabilities","mswmdm/IWMDMStorageGlobals::GetCapabilities","wmdm.iwmdmstorageglobals_getcapabilities"]
old-location: wmdm\iwmdmstorageglobals_getcapabilities.htm
tech.root: WMDM
ms.assetid: 0eea5448-f43d-4181-a497-476957fa7a08
ms.date: 12/05/2018
ms.keywords: GetCapabilities, GetCapabilities method [windows Media Device Manager], GetCapabilities method [windows Media Device Manager],IWMDMStorageGlobals interface, IWMDMStorageGlobals interface [windows Media Device Manager],GetCapabilities method, IWMDMStorageGlobals.GetCapabilities, IWMDMStorageGlobals::GetCapabilities, IWMDMStorageGlobalsGetCapabilities, mswmdm/IWMDMStorageGlobals::GetCapabilities, wmdm.iwmdmstorageglobals_getcapabilities
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
 - IWMDMStorageGlobals::GetCapabilities
 - mswmdm/IWMDMStorageGlobals::GetCapabilities
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
 - IWMDMStorageGlobals.GetCapabilities
---

# IWMDMStorageGlobals::GetCapabilities


## -description

The <b>GetCapabilities</b> method retrieves the capabilities of the root storage medium.

## -parameters

### -param pdwCapabilities [out]

Pointer to a <b>DWORD</b> containing a bitwise <b>OR</b> of zero or more of the following values.

<table>
<tr>
<th>Capability code
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_STORAGECAP_FOLDERSINROOT</td>
<td>The medium supports folders in the root of storage.</td>
</tr>
<tr>
<td>WMDM_STORAGECAP_FILESINROOT</td>
<td>The medium supports files in the root of storage.</td>
</tr>
<tr>
<td>WMDM_STORAGECAP_FOLDERSINFOLDERS</td>
<td>The medium supports nested folders.</td>
</tr>
<tr>
<td>WMDM_STORAGECAP_FILESINFOLDERS</td>
<td>The medium supports files in folders.</td>
</tr>
<tr>
<td>WMDM_STORAGECAP_FOLDERLIMITEXISTS</td>
<td>There is an arbitrary count limit for the number of folders allowed per the form of folder support by the medium.</td>
</tr>
<tr>
<td>WMDM_STORAGECAP_FILELIMITEXISTS</td>
<td>There is an arbitrary count limit for the number of files allowed per the form of file support by the medium.</td>
</tr>
<tr>
<td>WMDM_STORAGECAP_NOT_INITIALIZABLE</td>
<td>The medium can not be initialized. The top-level storage can be formatted by default.</td>
</tr>
</table>

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals Interface</a>