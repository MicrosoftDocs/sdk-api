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

# ISyncMgrSynchronize::ShowProperties


## -description


Called by the synchronization manager when a user selects an item in the choice dialog box, and then clicks the <b>Properties</b> button.


## -parameters




### -param hWndParent [in]

Type: <b>HWND</b>

The parent <b>HWND</b> for any user interface that a registered application displays to set properties. This value can be <b>NULL</b>.


### -param ItemID [in]

Type: <b>REFGUID</b>

The item ID for properties that are requested.


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, and the following.

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
The properties dialog for an item is handled successfully.

</td>
</tr>
</table>
 




## -remarks



If a registered application provides a properties dialog box for an item, it must set the SYNCMGRITEM_HASPROPERTIES bit in the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/84fa1d81-d1b9-44d7-be97-14511ef95528">SYNCMGRITEM</a> structure.

If <i>ItemID</i> is GUID_NULL the handler should show the properties dialog for the overall handler.

The appearance of the displayed dialog box should be consistent with a standard property page dialog box.




## -see-also




<a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a>



<a href="https://msdn.microsoft.com/84fa1d81-d1b9-44d7-be97-14511ef95528">SYNCMGRITEM</a>



<a href="https://msdn.microsoft.com/6297f10b-9a2c-4077-9dca-e5c0850d125a">SYNCMGRITEMFLAGS</a>
 

 

