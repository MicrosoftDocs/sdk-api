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

# IMDSPObject::Open


## -description



The <b>Open</b> method opens the associated object and prepares it for <a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a> operations. This operation is valid only if the storage object represents a file.




## -parameters




### -param fuMode [in]

Mode in which the file must be opened. It must be one of the following two values.

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
<td>MDSP_READ</td>
<td>Query whether a subsequent call to <b>Read</b> would be allowed.</td>
</tr>
<tr>
<td>MDSP_WRITE</td>
<td>Query whether a subsequent call to <b>Insert</b> would be allowed.</td>
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



If the underlying file-system does not support opening of multiple files at the same time, the service provider should gracefully the return Win32 error code ERROR_TOO_MANY_OPEN_FILES, if the client attempts to open more than one file at a time.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/271d7185-1a9d-4bec-9289-4ae5461ed741">IMDSPObject Interface</a>



<a href="https://msdn.microsoft.com/453dbf9e-4b71-4ceb-80e2-eaa0cf4cd29d">IMDSPObject::Close</a>



<a href="https://msdn.microsoft.com/1acf4112-0cb8-47e4-b8dc-3e820c0ef72f">IMDSPObject::Read</a>



<a href="https://msdn.microsoft.com/89494180-9dd7-41f3-b510-a59c38415d75">IMDSPObject::Seek</a>



<a href="https://msdn.microsoft.com/29f16be5-9304-4b09-86e8-3f9e0e591a41">IMDSPObject::Write</a>
 

 

