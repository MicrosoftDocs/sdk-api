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

# _tagSYNCMGRPROGRESSITEM structure


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
 

 

