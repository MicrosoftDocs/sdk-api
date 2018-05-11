---
UID: NF:mobsync.ISyncMgrSynchronize.EnumSyncMgrItems
title: ISyncMgrSynchronize::EnumSyncMgrItems
author: windows-driver-content
description: Obtains the ISyncMgrEnumItems interface for the items that are handled by a registered application.
old-location: shell\syncmgr_isyncmgrsynchronize_enumsyncmgritems.htm
old-project: shell
ms.assetid: 75f6ce68-237f-4228-adcf-f5ec929f49a7
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: EnumSyncMgrItems, EnumSyncMgrItems method [Windows Shell], EnumSyncMgrItems method [Windows Shell],ISyncMgrSynchronize interface, ISyncMgrSynchronize interface [Windows Shell],EnumSyncMgrItems method, ISyncMgrSynchronize.EnumSyncMgrItems, ISyncMgrSynchronize::EnumSyncMgrItems, mobsync/ISyncMgrSynchronize::EnumSyncMgrItems, shell.syncmgr_isyncmgrsynchronize_enumsyncmgritems, syncmgr.isyncmgrsynchronize_enumsyncmgritems
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
-	ISyncMgrSynchronize.EnumSyncMgrItems
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
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
 

 

