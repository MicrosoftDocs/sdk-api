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

# IMDSPDevice3::FindStorage


## -description



The <b>FindStorage</b> method finds a storage with the given persistent unique identifier. The persistent unique identifier of a storage is described by the <b>g_wszWMDMPersistentUniqueID</b> property of that storage.




## -parameters




### -param findScope [in]

Scope of the find operation. It must be one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>WMDM_FIND_SCOPE_GLOBAL</td>
<td>Search the whole device.</td>
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
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The service provider returns a persistent unique identifier through the <b>g_wszWMDMPersistentUniqueID</b> property of the storage. For a specific storage, the persistent unique identifier supplied by service provider should be same across different device connect sessions.

The application may call <b>FindStorage</b> with this persistent unique identifier at a later point. In response, Windows Media Device Manager calls this method on the service provider (SP).

A persistent unique identifier is used to uniquely identify content stored on a particular device. It does not represent a content-specific globally unique identifier that remains identical across all devices. Thus, the same content stored in different storages will have different persistent unique identifiers.

Windows Media Device Manager calls this method only for devices that are registered to enable synchronization with Windows Media Player. For more information, see <a href="https://msdn.microsoft.com/a312dfef-ac48-4c58-a59a-b277f5386419">Enabling Synchronization with Windows Media Player</a>.




## -see-also




<a href="https://msdn.microsoft.com/a312dfef-ac48-4c58-a59a-b277f5386419">Enabling Synchronization with Windows Media Player</a>



<a href="https://msdn.microsoft.com/919c26f4-6954-462a-8b4a-530e78bb72e6">IMDSPDevice3 Interface</a>



<a href="https://msdn.microsoft.com/a341289b-79e6-4ac7-b0d3-72ad5953c1df">IMDSPStorage3::GetMetadata</a>



<a href="https://msdn.microsoft.com/024a295a-ab23-4ee8-963b-1c18e244627a">IMDSPStorage4::FindStorage</a>



<a href="https://msdn.microsoft.com/0f7b3a68-97b3-4470-8ca8-e8eb8a5f83b7">IMDSPStorage4::GetSpecifiedMetadata</a>



<a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>



<a href="https://msdn.microsoft.com/971f84d5-8383-4b38-a201-b21100b2f37e">WMDM_FIND_SCOPE</a>
 

 

