---
UID: NF:emptyvc.IEmptyVolumeCache.Purge
title: IEmptyVolumeCache::Purge (emptyvc.h)
description: Notifies the handler to start deleting its unneeded files.
helpviewer_keywords: ["IEmptyVolumeCache interface [Legacy Windows Environment Features]","Purge method","IEmptyVolumeCache.Purge","IEmptyVolumeCache::Purge","Purge","Purge method [Legacy Windows Environment Features]","Purge method [Legacy Windows Environment Features]","IEmptyVolumeCache interface","_win32_IEmptyVolumeCache_Purge","emptyvc/IEmptyVolumeCache::Purge","lwef.iemptyvolumecache_purge","shell.iemptyvolumecache_purge"]
old-location: lwef\iemptyvolumecache_purge.htm
tech.root: lwef
ms.assetid: c42430da-9d6a-42e9-bc4f-325d986c7c48
ms.date: 12/05/2018
ms.keywords: IEmptyVolumeCache interface [Legacy Windows Environment Features],Purge method, IEmptyVolumeCache.Purge, IEmptyVolumeCache::Purge, Purge, Purge method [Legacy Windows Environment Features], Purge method [Legacy Windows Environment Features],IEmptyVolumeCache interface, _win32_IEmptyVolumeCache_Purge, emptyvc/IEmptyVolumeCache::Purge, lwef.iemptyvolumecache_purge, shell.iemptyvolumecache_purge
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
 - IEmptyVolumeCache::Purge
 - emptyvc/IEmptyVolumeCache::Purge
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
 - IEmptyVolumeCache.Purge
---

# IEmptyVolumeCache::Purge


## -description

Notifies the handler to start deleting its unneeded files.

## -parameters

### -param dwlSpaceToFree [in]

Type: <b>DWORDLONG</b>

The amount of disk space that the handler should free. If this parameter is set to -1, the handler should delete all its files.

### -param picb [in]

Type: <b>IEmptyVolumeCacheCallback*</b>

A pointer to the disk cleanup manager's <a href="/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecachecallback">IEmptyVolumeCacheCallBack</a> interface. This pointer can be used to call the interface's <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecachecallback-purgeprogress">PurgeProgress</a> method to report on the progress of the operation.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The operation was ended prematurely. This value is usually returned when <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecachecallback-purgeprogress">PurgeProgress</a> returns E_ABORT. This typically happens when the user cancels the operation by clicking the disk cleanup manager's <b>Cancel</b> button.

</td>
</tr>
</table>

## -remarks

For Windows 98, the <i>dwSpaceToFree</i> parameter is always set to the value specified by the handler when <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused">IEmptyVolumeCache::GetSpaceUsed</a> was called.

In general, handlers should be kept simple and delete all of their files when this function is called. If there are significant performance advantages to only deleting a portion of the files, the handler should implement the <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-showproperties">ShowProperties</a> method. When called, this method displays a UI that allows the user to select the files to be deleted.