---
UID: NF:syncmgr.ISyncMgrConflict.GetConflictIdInfo
title: ISyncMgrConflict::GetConflictIdInfo
author: windows-sdk-content
description: Gets information that identifies a conflict within a conflict store.
old-location: shell\ISyncMgrConflict_GetConflictIdInfo.htm
tech.root: shell
ms.assetid: 9686a6e5-5a0a-4520-803e-1660676d9f61
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetConflictIdInfo, GetConflictIdInfo method [Windows Shell], GetConflictIdInfo method [Windows Shell],ISyncMgrConflict interface, ISyncMgrConflict interface [Windows Shell],GetConflictIdInfo method, ISyncMgrConflict.GetConflictIdInfo, ISyncMgrConflict::GetConflictIdInfo, _shell_ISyncMgrConflict_GetConflictIdInfo, shell.ISyncMgrConflict_GetConflictIdInfo, syncmgr/ISyncMgrConflict::GetConflictIdInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
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
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrConflict.GetConflictIdInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrConflict::GetConflictIdInfo


## -description


Gets information that identifies a conflict within a conflict store.


## -parameters




### -param pConflictIdInfo [out]

Type: <b><a href="https://msdn.microsoft.com/9a54ef7e-0b22-436e-891b-80610ddaef00">SYNCMGR_CONFLICT_ID_INFO</a>*</b>

A pointer to a conflict ID info structure. See <a href="https://msdn.microsoft.com/9a54ef7e-0b22-436e-891b-80610ddaef00">SYNCMGR_CONFLICT_ID_INFO</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  Each member should be allocated using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. Free each member using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.</div>
<div> </div>
This method contains two opaque blobs: One is the ID uniquely identifying a conflict within a conflict store. The other is optional extra information stored with the conflict that may be used by the implementation when creating conflict objects in <a href="https://msdn.microsoft.com/86414360-7dc5-4819-8372-0cede07ba41b">BindToConflict</a> and <a href="https://msdn.microsoft.com/d6fbb322-7bb0-4ad0-bf01-2fe407689fe5">RemoveConflicts</a>.

The size of of the ID blob must be kept short so that the ID may be embedded inside the conflict's pointer to an item identifier list (PIDL) or parsing name.



