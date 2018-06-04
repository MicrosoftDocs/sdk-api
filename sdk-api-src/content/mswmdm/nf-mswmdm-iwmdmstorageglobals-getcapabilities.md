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

# IWMDMStorageGlobals::GetCapabilities


## -description



The <b>GetCapabilities</b> method retrieves the capabilities of the root storage medium.




## -parameters




### -param pdwCapabilities [out]

Pointer to a <b>DWORD</b> containing a bitwise <b>OR</b> of zero or more of the following values.

<table>
<tr>
<th>
                  Capability code
                </th>
<th>
                  Description
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
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/fe164271-58f0-4b28-a200-6b15f8b42d36">IWMDMStorageGlobals Interface</a>
 

 

