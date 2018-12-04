---
UID: NF:mswmdm.IMDSPObject.Seek
title: IMDSPObject::Seek
author: windows-sdk-content
description: The Seek method sets the current position within the object. This operation is valid only if the storage object represents a file.
old-location: wmdm\imdspobject_seek.htm
tech.root: WMDM
ms.assetid: 89494180-9dd7-41f3-b510-a59c38415d75
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IMDSPObject interface [windows Media Device Manager],Seek method, IMDSPObject.Seek, IMDSPObject::Seek, IMDSPObjectSeek, Seek, Seek method [windows Media Device Manager], Seek method [windows Media Device Manager],IMDSPObject interface, mswmdm/IMDSPObject::Seek, wmdm.imdspobject_seek
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
 - IMDSPObject.Seek
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPObject::Seek


## -description



The <b>Seek</b> method sets the current position within the object. This operation is valid only if the storage object represents a file.




## -parameters




### -param fuFlags [in]

Mode in which the file must be opened. It must be one of the values in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>MDSP_SEEK_BOF</td>
<td>Seek <i>dwOffset</i> bytes forward from the beginning of the file.</td>
</tr>
<tr>
<td>MDSP_SEEK_CUR</td>
<td>Seek <i>dwOffset</i> bytes forward from the current position.</td>
</tr>
<tr>
<td>MDSP_SEEK_EOF</td>
<td>Seek <i>dwOffset</i> bytes backward from the end of the file.</td>
</tr>
</table>
 


### -param dwOffset [in]

<b>DWORD</b> containing the number of bytes to seek.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/271d7185-1a9d-4bec-9289-4ae5461ed741">IMDSPObject Interface</a>



<a href="https://msdn.microsoft.com/9e54bcbd-4f14-49e0-8211-2f79f024c80a">IMDSPObject::Open</a>



<a href="https://msdn.microsoft.com/1acf4112-0cb8-47e4-b8dc-3e820c0ef72f">IMDSPObject::Read</a>
 

 

