---
UID: NF:mswmdm.IMDSPStorage4.FindStorage
title: IMDSPStorage4::FindStorage
author: windows-sdk-content
description: The FindStorage method finds a storage with the given persistent unique identifier. The persistent unique identifier of a storage is described by the g_wszWMDMPersistentUniqueID property of that storage.
old-location: wmdm\imdspstorage4_findstorage.htm
tech.root: WMDM
ms.assetid: 024a295a-ab23-4ee8-963b-1c18e244627a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FindStorage, FindStorage method [windows Media Device Manager], FindStorage method [windows Media Device Manager],IMDSPStorage4 interface, IMDSPStorage4 interface [windows Media Device Manager],FindStorage method, IMDSPStorage4.FindStorage, IMDSPStorage4::FindStorage, IMDSPStorage4FindStorage, mswmdm/IMDSPStorage4::FindStorage, wmdm.imdspstorage4_findstorage
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPStorage4.FindStorage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPStorage4::FindStorage


## -description



The <b>FindStorage</b> method finds a storage with the given persistent unique identifier. The persistent unique identifier of a storage is described by the <b>g_wszWMDMPersistentUniqueID</b> property of that storage.




## -parameters




### -param findScope [in]

Scope of the find operation. It must be one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_FIND_SCOPE_GLOBAL</td>
<td>Search the entire device.</td>
</tr>
<tr>
<td>WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN</td>
<td>Search only in the immediate children of the current storage.</td>
</tr>
</table>
 


### -param pwszUniqueID [in]

Persistent unique identifier of the storage.


### -param ppStorage [out]

Pointer to the returned storage specified by the <i>pwszUniqueID</i> parameter.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The service provider returns a persistent unique identifier through the <b>g_wszWMDMPersistentUniqueID</b> property of the storage. For a specific storage, the persistent unique identifier supplied by service provider should be the same across different device connect sessions.

The application may call <b>FindStorage</b> with this persistent unique identifier at a later point. In response, Windows Media Device Manager calls this method on the service provider.

A persistent unique identifier is used to uniquely identify content stored on a particular device. It does not represent a content-specific globally unique identifier that remains identical across all devices. Thus, the same content stored in different storages will have different persistent unique identifiers.

This method allows searching for a storage based on persistent unique identifier while <b>IMDSPStorage2::GetStorage</b> allows searching for a storage based on name.

Windows Media Device Manager calls this method only for devices that can be synchronized with Windows Media Player. See <a href="https://msdn.microsoft.com/a312dfef-ac48-4c58-a59a-b277f5386419">Enabling Synchronization with Windows Media Player</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/a312dfef-ac48-4c58-a59a-b277f5386419">Enabling Synchronization with Windows Media Player</a>



<a href="https://msdn.microsoft.com/2ddfdfc8-db43-4acc-aebc-617d3e746a4f">IMDSPStorage2::GetStorage</a>



<a href="https://msdn.microsoft.com/c1236acc-1f11-4501-9374-2486f7d61db3">IMDSPStorage4 Interface</a>
 

 

