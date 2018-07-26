---
UID: NF:shobjidl_core.IFileSyncMergeHandler.ShowResolveConflictUIAsync
title: IFileSyncMergeHandler::ShowResolveConflictUIAsync
author: windows-sdk-content
description: IFileSyncMergeHandler::ShowResolveConflictUIAsync method
old-location: shell\IFileSyncMergeHandler_ShowResolveConflictUIAsync.htm
old-project: shell
ms.assetid: 7D437A9A-8F16-4E5E-B464-61A9A398C649
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IFileSyncMergeHandler interface [Windows Shell],ShowResolveConflictUIAsync method, IFileSyncMergeHandler.ShowResolveConflictUIAsync, IFileSyncMergeHandler::ShowResolveConflictUIAsync, MUS_COMPLETE, MUS_FAILED, MUS_USERINPUTNEEDED, ShowResolveConflictUIAsync, ShowResolveConflictUIAsync method [Windows Shell], ShowResolveConflictUIAsync method [Windows Shell],IFileSyncMergeHandler interface, shell.IFileSyncMergeHandler_ShowResolveConflictUIAsync, shobjidl_core/IFileSyncMergeHandler::ShowResolveConflictUIAsync
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileSyncMergeHandler.ShowResolveConflictUIAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileSyncMergeHandler::ShowResolveConflictUIAsync


## -description




## -parameters




### -param localFilePath [in]

Type: <b>LPCWSTR</b>


### -param monitorToDisplayOn [in]

Type: <b>HMONITOR</b>


#### - updateStatus [out]

Type: <b>MERGE_UPDATE_STATUS*</b>



#### MUS_COMPLETE



#### MUS_USERINPUTNEEDED



#### MUS_FAILED


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/467BF7B9-184E-409F-B5B7-F95E9891C2CD">IFileSyncMergeHandler</a>
 

 

