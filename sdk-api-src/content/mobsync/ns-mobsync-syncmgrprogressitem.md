---
UID: NS:mobsync._tagSYNCMGRPROGRESSITEM
title: SYNCMGRPROGRESSITEM (mobsync.h)
author: windows-sdk-content
description: Provides status information while a synchronization is in progress. This structure is used with the ISyncMgrSynchronizeCallback::Progress method and corresponds to a single synchronization item.
old-location: shell\syncmgr_syncmgrprogressitem.htm
tech.root: shell
ms.assetid: 94ac1206-be5f-467c-ab4a-11f574c406ca
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPSYNCMGRPROGRESSITEM, LPSYNCMGRPROGRESSITEM, LPSYNCMGRPROGRESSITEM structure pointer [Windows Shell], SYNCMGRPROGRESSITEM, SYNCMGRPROGRESSITEM structure [Windows Shell], mobsync/LPSYNCMGRPROGRESSITEM, mobsync/SYNCMGRPROGRESSITEM, shell.syncmgr_syncmgrprogressitem, syncmgr.syncmgrprogressitem"
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mobsync.h
api_name:
 - SYNCMGRPROGRESSITEM
product: Windows
targetos: Windows
req.typenames: SYNCMGRPROGRESSITEM, *LPSYNCMGRPROGRESSITEM
req.redist: 
---

# SYNCMGRPROGRESSITEM structure


## -description


Provides status information while a synchronization is in progress. This structure is used with the <a href="https://msdn.microsoft.com/924310aa-e210-476d-b532-f235de943498">ISyncMgrSynchronizeCallback::Progress</a> method and corresponds to a single synchronization item.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes.


### -field mask

Type: <b>UINT</b>

Flags from the <a href="https://msdn.microsoft.com/a2bdc883-2e61-42a4-a88b-8fab42f018e1">SYNCMGRSTATUS</a> enumeration that specify which members of this structure are used.


### -field lpcStatusText

Type: <b>LPCWSTR</b>

Status text.


### -field dwStatusType

Type: <b>DWORD</b>

One of the values from the <a href="https://msdn.microsoft.com/a2bdc883-2e61-42a4-a88b-8fab42f018e1">SYNCMGRSTATUS</a> enumeration.


### -field iProgValue

Type: <b>int</b>

An integer that indicates the progress value.


### -field iMaxValue

Type: <b>int</b>

An integer that indicates the maximum progress value.


## -see-also




<a href="https://msdn.microsoft.com/924310aa-e210-476d-b532-f235de943498">ISyncMgrSynchronizeCallback::Progress</a>
 

 

