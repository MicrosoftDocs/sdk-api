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

# ISyncMgrSynchronize::EnumSyncMgrItems


## -description


Obtains the 
<a href="https://msdn.microsoft.com/d90e3a19-0ea8-4396-a6e7-dafe1dc9b2ec">ISyncMgrEnumItems</a> interface for the items that are handled by a registered application.


## -parameters




### -param ppSyncMgrEnumItems [out]

Type: <b><a href="https://msdn.microsoft.com/d90e3a19-0ea8-4396-a6e7-dafe1dc9b2ec">ISyncMgrEnumItems</a>**</b>

The address of the variable that receives a pointer to a valid 
<a href="https://msdn.microsoft.com/d90e3a19-0ea8-4396-a6e7-dafe1dc9b2ec">ISyncMgrEnumItems</a> interface.


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, and the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The enumeration interface is returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_SYNCMGR_MISSINGITEMS</b></dt>
</dl>
</td>
<td width="60%">
The enumeration interface object is returned successfully, but some items are missing. When this success code is returned, the synchronization manager does not remove any stored preferences for ItemIds that are not returned in the enumerator.

</td>
</tr>
</table>
 




## -remarks



The enumeration object that this method creates implements the 
<a href="https://msdn.microsoft.com/d90e3a19-0ea8-4396-a6e7-dafe1dc9b2ec">ISyncMgrEnumItems</a> interface, which is a standard enumeration interface that contains the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/d90e3a19-0ea8-4396-a6e7-dafe1dc9b2ec">ISyncMgrEnumItems</a>



<a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a>
 

 

