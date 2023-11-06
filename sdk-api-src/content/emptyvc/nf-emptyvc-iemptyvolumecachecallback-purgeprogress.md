---
UID: NF:emptyvc.IEmptyVolumeCacheCallBack.PurgeProgress
title: IEmptyVolumeCacheCallBack::PurgeProgress (emptyvc.h)
description: Called periodically by a disk cleanup handler to update the disk cleanup manager on the progress of a purge of deletable files.
helpviewer_keywords: ["EVCCBF_LASTNOTIFICATION","IEmptyVolumeCacheCallBack interface [Legacy Windows Environment Features]","PurgeProgress method","IEmptyVolumeCacheCallBack.PurgeProgress","IEmptyVolumeCacheCallBack::PurgeProgress","PurgeProgress","PurgeProgress method [Legacy Windows Environment Features]","PurgeProgress method [Legacy Windows Environment Features]","IEmptyVolumeCacheCallBack interface","_win32_IEmptyVolumeCacheCallBack_PurgeProgress","emptyvc/IEmptyVolumeCacheCallBack::PurgeProgress","lwef.iemptyvolumecachecallback_purgeprogress","shell.iemptyvolumecachecallback_purgeprogress"]
old-location: lwef\iemptyvolumecachecallback_purgeprogress.htm
tech.root: lwef
ms.assetid: 96b97919-9b3b-418e-a76a-a2e8aad453b9
ms.date: 12/05/2018
ms.keywords: EVCCBF_LASTNOTIFICATION, IEmptyVolumeCacheCallBack interface [Legacy Windows Environment Features],PurgeProgress method, IEmptyVolumeCacheCallBack.PurgeProgress, IEmptyVolumeCacheCallBack::PurgeProgress, PurgeProgress, PurgeProgress method [Legacy Windows Environment Features], PurgeProgress method [Legacy Windows Environment Features],IEmptyVolumeCacheCallBack interface, _win32_IEmptyVolumeCacheCallBack_PurgeProgress, emptyvc/IEmptyVolumeCacheCallBack::PurgeProgress, lwef.iemptyvolumecachecallback_purgeprogress, shell.iemptyvolumecachecallback_purgeprogress
req.header: emptyvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEmptyVolumeCacheCallBack::PurgeProgress
 - emptyvc/IEmptyVolumeCacheCallBack::PurgeProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IEmptyVolumeCacheCallBack.PurgeProgress
---

# IEmptyVolumeCacheCallBack::PurgeProgress


## -description

Called periodically by a disk cleanup handler to update the disk cleanup manager on the progress of a purge of deletable files.

## -parameters

### -param dwlSpaceFreed [in]

Type: <b>DWORDLONG</b>

The amount of disk space, in bytes, that has been freed at this point in the purge. The disk cleanup manager uses this value to update its progress bar.

### -param dwlSpaceToFree [in]

Type: <b>DWORDLONG</b>

The amount of disk space, in bytes, that remains to be freed at this point in the purge.

### -param dwFlags [in]

Type: <b>DWORD</b>

A flag that can be sent to the disk cleanup manager. It can have the following value: 



#### EVCCBF_LASTNOTIFICATION

This flag should be set if the handler will not call this method again. It is typically set when the purge is near completion.

### -param pcwszStatus [in]

Type: <b>LPCWSTR</b>

Reserved.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The handler should continue purging deletable files.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
This value is returned when the user clicks the <b>Cancel</b> button on the disk cleanup manager's dialog box while a scan is in progress. The handler should stop purging files and shut down.

</td>
</tr>
</table>

## -remarks

This method is typically called by the handler's <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-purge">Purge</a> method while the handler is purging deletable files. Handlers should call <b>PurgeProgress</b> periodically to keep the user informed of progress, especially if the purge will take a long time. Calling this method frequently also allows the handler to shut down promptly if a user cancels a purge.