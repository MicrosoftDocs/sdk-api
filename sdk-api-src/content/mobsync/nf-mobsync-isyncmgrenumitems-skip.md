---
UID: NF:mobsync.ISyncMgrEnumItems.Skip
title: ISyncMgrEnumItems::Skip
author: windows-sdk-content
description: Instructs the enumerator to skip the next celt elements in the enumeration so that the next call to ISyncMgrEnumItems::Next does not return those elements.
old-location: shell\syncmgr_isyncmgrenumitems_skip.htm
old-project: shell
ms.assetid: f317306b-5317-4c5e-a5e6-fd2d8728bc52
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ISyncMgrEnumItems interface [Windows Shell],Skip method, ISyncMgrEnumItems.Skip, ISyncMgrEnumItems::Skip, Skip, Skip method [Windows Shell], Skip method [Windows Shell],ISyncMgrEnumItems interface, mobsync/ISyncMgrEnumItems::Skip, shell.syncmgr_isyncmgrenumitems_skip, syncmgr.isyncmgrenumitems_skip
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
 - ISyncMgrEnumItems.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISyncMgrEnumItems::Skip


## -description


Instructs the enumerator to skip the next <i>celt</i> elements in the enumeration so that the next call to <a href="https://msdn.microsoft.com/bb4ab08a-aa12-46f0-8c7d-82742b0b1538">ISyncMgrEnumItems::Next</a> does not return those elements.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of items to skip.


## -returns



Type: <b>HRESULT</b>

Return S_OK if the method succeeds.



