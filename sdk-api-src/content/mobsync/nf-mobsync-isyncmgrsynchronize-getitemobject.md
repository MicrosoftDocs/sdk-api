---
UID: NF:mobsync.ISyncMgrSynchronize.GetItemObject
title: ISyncMgrSynchronize::GetItemObject
author: windows-sdk-content
description: Obtains an interface on a specified item that a registered application handles.
old-location: shell\syncmgr_isyncmgrsynchronize_getitemobject.htm
old-project: shell
ms.assetid: e21e1cd5-ab15-42e3-b3c7-1ae0c4dfec02
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetItemObject, GetItemObject method [Windows Shell], GetItemObject method [Windows Shell],ISyncMgrSynchronize interface, ISyncMgrSynchronize interface [Windows Shell],GetItemObject method, ISyncMgrSynchronize.GetItemObject, ISyncMgrSynchronize::GetItemObject, mobsync/ISyncMgrSynchronize::GetItemObject, shell.syncmgr_isyncmgrsynchronize_getitemobject, syncmgr.isyncmgrsynchronize_getitemobject
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SYNCMGRSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronize.GetItemObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISyncMgrSynchronize::GetItemObject


## -description


Obtains an interface on a specified item that a registered application handles.


## -parameters




### -param ItemID [in]

Type: <b>REFGUID</b>

An identifier for a requested item.


### -param riid [in]

Type: <b>REFIID</b>

An identifier for a requested interface.


### -param ppv [out]

Type: <b>void**</b>

An address of a variable that receives a pointer to a requested interface.


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The requested interface is not found.

</td>
</tr>
</table>
 




## -remarks



This method exists only for forward compatibility. Currently, there are no interfaces defined on an item. Application implementers must return E_NOTIMPL from this method.




## -see-also




<a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a>
 

 

