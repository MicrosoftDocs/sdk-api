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

# IMDSPStorage::GetAttributes


## -description



The <b>GetAttributes</b> method retrieves the attributes of this storage object.




## -parameters




### -param pdwAttributes [out]

Pointer to a <b>DWORD</b> containing the attributes as defined by in the <b>IWMDMStorage::GetAttributes</b> method.


### -param pFormat [out]

Pointer to a <b>_WAVEFORMATEX</b> structure that is filled with attribute information about the object.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



Evaluation of attributes is a crucial step when exposing the contents of the media device. Devices may not support hierarchical storage of data on storage media. The <b>GetAttributes</b> method allows the application to infer the support and format of the file system by discovering its structure through object attributes.

For example, the attributes of a top-level <b>IMDSPStorage</b> interface indicate a storage medium, and <b>IMDSPEnumStorage</b> exposes the contents of the medium. For an .mp3 file, the attributes indicate a file whose type can be determined by further examination of both the attributes and the file name. In a hierarchical medium, the attributes can indicate a directory whose contents can be exposed by <b>IMDSPStorage::EnumStorage</b>.

The <b>_WAVEFORMATEX</b> parameter is optional. If you pass a valid <b>_WAVEFORMATEX</b> pointer to an audio file, <b>GetAttributes</b> passes descriptive information back into the structure. However, if the file is not audio, the <b>_WAVEFORMATEX</b> parameter is ignored.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/fc2fed46-1f4d-4d53-a843-0f699b687a18">IMDSPEnumStorage Interface</a>



<a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage Interface</a>



<a href="https://msdn.microsoft.com/2db30715-cd49-4e55-b0d0-73ac531f8661">IMDSPStorage2::GetAttributes2</a>



<a href="https://msdn.microsoft.com/e995b255-364f-4ea6-b7fd-4443e84432ef">IMDSPStorage::SetAttributes</a>



<a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a>
 

 

