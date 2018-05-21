---
UID: NF:mobsync.ISyncMgrSynchronize.ShowProperties
title: ISyncMgrSynchronize::ShowProperties
author: windows-driver-content
description: Called by the synchronization manager when a user selects an item in the choice dialog box, and then clicks the Properties button.
old-location: shell\syncmgr_isyncmgrsynchronize_showproperties.htm
old-project: shell
ms.assetid: 5587cc8a-b359-483e-98ba-82f1bbe058d8
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ISyncMgrSynchronize interface [Windows Shell],ShowProperties method, ISyncMgrSynchronize.ShowProperties, ISyncMgrSynchronize::ShowProperties, ShowProperties, ShowProperties method [Windows Shell], ShowProperties method [Windows Shell],ISyncMgrSynchronize interface, mobsync/ISyncMgrSynchronize::ShowProperties, shell.syncmgr_isyncmgrsynchronize_showproperties, syncmgr.isyncmgrsynchronize_showproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SYNCMGRSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mobsync.dll
api_name:
-	ISyncMgrSynchronize.ShowProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
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
 

 

