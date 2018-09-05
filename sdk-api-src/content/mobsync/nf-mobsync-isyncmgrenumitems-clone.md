---
UID: NF:mobsync.ISyncMgrEnumItems.Clone
title: ISyncMgrEnumItems::Clone
author: windows-sdk-content
description: Creates another items enumerator with the same state as the current enumerator to iterate over the same list. This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time.
old-location: shell\syncmgr_isyncmgrenumitems_clone.htm
old-project: shell
ms.assetid: 33bf4956-3d16-412c-9551-4ae3366ddd78
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: Clone, Clone method [Windows Shell], Clone method [Windows Shell],ISyncMgrEnumItems interface, ISyncMgrEnumItems interface [Windows Shell],Clone method, ISyncMgrEnumItems.Clone, ISyncMgrEnumItems::Clone, mobsync/ISyncMgrEnumItems::Clone, shell.syncmgr_isyncmgrenumitems_clone, syncmgr.isyncmgrenumitems_clone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mobsync.h
req.include-header: 
req.redist: 
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
 - ISyncMgrEnumItems.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISyncMgrEnumItems::Clone


## -description


Creates another items enumerator with the same state as the current enumerator to iterate over the same list. This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time.


## -parameters




### -param ppenum






#### - ISyncMgrEnumItems [out]

Type: <b>ppenum**</b>

The address of a variable that receives the <a href="https://msdn.microsoft.com/d90e3a19-0ea8-4396-a6e7-dafe1dc9b2ec">ISyncMgrEnumItems</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

Return S_OK if the method succeeds.




## -remarks



The calling application must release the new enumerator separately from the first enumerator.



