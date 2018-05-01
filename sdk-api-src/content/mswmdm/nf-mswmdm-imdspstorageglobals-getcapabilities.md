---
UID: NF:mswmdm.IMDSPStorageGlobals.GetCapabilities
title: IMDSPStorageGlobals::GetCapabilities method
author: windows-driver-content
description: The GetCapabilities method retrieves the capabilities of the storage medium that an instance of this interface is associated with.
old-location: wmdm\imdspstorageglobals_getcapabilities.htm
old-project: WMDM
ms.assetid: 83204c04-503d-4687-8a4d-3c95a6def8d1
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: GetCapabilities method [windows Media Device Manager], GetCapabilities method [windows Media Device Manager], IMDSPStorageGlobals interface, GetCapabilities,IMDSPStorageGlobals.GetCapabilities, IMDSPStorageGlobals, IMDSPStorageGlobals interface [windows Media Device Manager], GetCapabilities method, IMDSPStorageGlobals::GetCapabilities, IMDSPStorageGlobalsGetCapabilities, mswmdm/IMDSPStorageGlobals::GetCapabilities, wmdm.imdspstorageglobals_getcapabilities
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
-	IMDSPStorageGlobals.GetCapabilities
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMDSPStorageGlobals::GetCapabilities method


## -description



The <b>GetCapabilities</b> method retrieves the capabilities of the storage medium that an instance of this interface is associated with.




## -parameters




### -param pdwCapabilities [out]

Pointer to a <b>DWORD</b> containing the capabilities of the storage medium.

The following flags can be returned in the <i>pdwCapabilities</i> parameter.

<table>
<tr>
<th>
                  Flag
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
<td>The medium supports folders in folders.</td>
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
<td>The medium cannot be initialized. By default, the top-level storage can be initialized.</td>
</tr>
</table>
 

For secured device implementations, the following flags describing the rights capabilities of the medium can also be returned.

<table>
<tr>
<th>
                  Flag
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>WMDM_RIGHTS_PLAYBACKCOUNT</td>
<td>The medium supports playback count limiting for content.</td>
</tr>
<tr>
<td>WMDM_RIGHTS_EXPIRATIONDATE</td>
<td>The medium supports expiration date tracking for content.</td>
</tr>
<tr>
<td>WMDM_RIGHTS_FREESERIALIDS</td>
<td>The medium supports a free serial identifier for the file.</td>
</tr>
<tr>
<td>WMDM_RIGHTS_GROUPID</td>
<td>The medium supports a group identifier for the file.</td>
</tr>
<tr>
<td>WMDM_RIGHTS_NAMEDSERIALIDS</td>
<td>The medium supports a named serial identifier for the file.</td>
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




## -remarks



Attempts to perform unsupported operations on the storage medium with the <b>IMDSPObject</b> interface return an error code. The <b>GetCapabilities</b> method can be called in order to determine whether an operation can be expected to succeed under normal circumstances.

If either the WMDM_STORAGECAP_FILELIMITEXISTS flag or the WMDM_STORAGECAP_FOLDERLIMITEXISTS flag is true, there are arbitrary limits on the number of files or folders that can be created. Operations through the <b>IMDSPObject</b> interface that exceed these limits will fail.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/70653352-a467-4197-93e3-e8fb45f99d34">IMDSPStorageGlobals Interface</a>
 

 

