---
UID: NF:emptyvc.IEmptyVolumeCache.GetSpaceUsed
title: IEmptyVolumeCache::GetSpaceUsed (emptyvc.h)
description: Requests the amount of disk space that the disk cleanup handler can free.
helpviewer_keywords: ["GetSpaceUsed","GetSpaceUsed method [Legacy Windows Environment Features]","GetSpaceUsed method [Legacy Windows Environment Features]","IEmptyVolumeCache interface","IEmptyVolumeCache interface [Legacy Windows Environment Features]","GetSpaceUsed method","IEmptyVolumeCache.GetSpaceUsed","IEmptyVolumeCache::GetSpaceUsed","_win32_IEmptyVolumeCache_GetSpaceUsed","emptyvc/IEmptyVolumeCache::GetSpaceUsed","lwef.iemptyvolumecache_getspaceused","shell.iemptyvolumecache_getspaceused"]
old-location: lwef\iemptyvolumecache_getspaceused.htm
tech.root: lwef
ms.assetid: c8ec2f70-f327-49d4-babb-a9640f105003
ms.date: 12/05/2018
ms.keywords: GetSpaceUsed, GetSpaceUsed method [Legacy Windows Environment Features], GetSpaceUsed method [Legacy Windows Environment Features],IEmptyVolumeCache interface, IEmptyVolumeCache interface [Legacy Windows Environment Features],GetSpaceUsed method, IEmptyVolumeCache.GetSpaceUsed, IEmptyVolumeCache::GetSpaceUsed, _win32_IEmptyVolumeCache_GetSpaceUsed, emptyvc/IEmptyVolumeCache::GetSpaceUsed, lwef.iemptyvolumecache_getspaceused, shell.iemptyvolumecache_getspaceused
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
 - IEmptyVolumeCache::GetSpaceUsed
 - emptyvc/IEmptyVolumeCache::GetSpaceUsed
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
 - IEmptyVolumeCache.GetSpaceUsed
---

# IEmptyVolumeCache::GetSpaceUsed


## -description

Requests the amount of disk space that the disk cleanup handler can free.

## -parameters

### -param pdwlSpaceUsed [out]

Type: <b>DWORDLONG*</b>

The amount of disk space, in bytes, that the handler can free. This value will be displayed in the disk cleanup manager's list, to the right of the handler's check box. To indicate that you do not know how much disk space can be freed, set this parameter to -1, and "???MB" will be displayed. If you set the <b>EVCF_DONTSHOWIFZERO</b> flag when <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-initialize">Initialize</a> was called, setting <i>pdwSpaceUsed</i> to zero will notify the disk cleanup manager to omit the handler from its list.

### -param picb [in]

Type: <b>IEmptyVolumeCacheCallback*</b>

A pointer to the disk cleanup manager's <a href="/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecachecallback">IEmptyVolumeCacheCallback</a> interface. This pointer can be used to call that interface's <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress">ScanProgress</a> method to report on the progress of the operation.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
An error occurred when the handler tried to calculate the amount of disk space that could be freed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The scan operation was ended prematurely. This value is usually returned when a call to <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress">ScanProgress</a> returns E_ABORT. This return value indicates that the user canceled the operation by clicking the disk cleanup manager's <b>Cancel</b> button.
          

</td>
</tr>
</table>

## -remarks

When this method is called by the disk cleanup manager, the handler should start scanning its files to determine which of them can be deleted, and how much disk space will be freed. Handlers should call <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress">IEmptyVolumeCache::ScanProgress</a> periodically to keep the user informed of the progress of the scan, especially if it will take a long time. Calling this method frequently also allows the handler to determine whether the user has canceled the operation. If <b>ScanProgress</b> returns E_ABORT, the user has canceled the scan. The handler should immediately stop scanning and return E_ABORT.
      

You should only set the <i>pdwSpaceUsed</i> parameter to -1 as a last resort. The handler is of limited value to a user if they don't know how much space will be freed.