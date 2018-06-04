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

# IMDSPStorage::GetName


## -description



The <b>GetName</b> method retrieves the display name of the storage object.




## -parameters




### -param pwszName [out]

Pointer to a (Unicode) wide-character null-terminated string containing the object name.


### -param nMaxChars [in]

Integer containing the maximum number of characters that can be copied to the name string.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The display name of the object is the file name without path information. In hierarchical media the display name would be concatenated with the ancestor instances of <b>IMDSPStorage</b> interfaces to create a full path-qualified name.

The <b>LPWSTR</b> string type is a 16-bit Unicode character string and does not accept byte-sized characters.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage Interface</a>



<a href="https://msdn.microsoft.com/4ba0c598-9ea2-42cc-a234-1c0e192971a8">IMDSPStorage::GetDate</a>



<a href="https://msdn.microsoft.com/95b28f9a-744c-4d49-a91c-6652d688b91a">IMDSPStorage::GetSize</a>
 

 

