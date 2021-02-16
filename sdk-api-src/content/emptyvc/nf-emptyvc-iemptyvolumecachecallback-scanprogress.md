---
UID: NF:emptyvc.IEmptyVolumeCacheCallBack.ScanProgress
title: IEmptyVolumeCacheCallBack::ScanProgress (emptyvc.h)
description: Called by a disk cleanup handler to update the disk cleanup manager on the progress of a scan for deletable files.
helpviewer_keywords: ["EVCCBF_LASTNOTIFICATION","IEmptyVolumeCacheCallBack interface [Legacy Windows Environment Features]","ScanProgress method","IEmptyVolumeCacheCallBack.ScanProgress","IEmptyVolumeCacheCallBack::ScanProgress","ScanProgress","ScanProgress method [Legacy Windows Environment Features]","ScanProgress method [Legacy Windows Environment Features]","IEmptyVolumeCacheCallBack interface","_win32_IEmptyVolumeCacheCallBack_ScanProgress","emptyvc/IEmptyVolumeCacheCallBack::ScanProgress","lwef.iemptyvolumecachecallback_scanprogress","shell.iemptyvolumecachecallback_scanprogress"]
old-location: lwef\iemptyvolumecachecallback_scanprogress.htm
tech.root: lwef
ms.assetid: 41ebc9db-d402-47d7-b303-f87357ae820d
ms.date: 12/05/2018
ms.keywords: EVCCBF_LASTNOTIFICATION, IEmptyVolumeCacheCallBack interface [Legacy Windows Environment Features],ScanProgress method, IEmptyVolumeCacheCallBack.ScanProgress, IEmptyVolumeCacheCallBack::ScanProgress, ScanProgress, ScanProgress method [Legacy Windows Environment Features], ScanProgress method [Legacy Windows Environment Features],IEmptyVolumeCacheCallBack interface, _win32_IEmptyVolumeCacheCallBack_ScanProgress, emptyvc/IEmptyVolumeCacheCallBack::ScanProgress, lwef.iemptyvolumecachecallback_scanprogress, shell.iemptyvolumecachecallback_scanprogress
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
 - IEmptyVolumeCacheCallBack::ScanProgress
 - emptyvc/IEmptyVolumeCacheCallBack::ScanProgress
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
 - IEmptyVolumeCacheCallBack.ScanProgress
---

# IEmptyVolumeCacheCallBack::ScanProgress


## -description

Called by a disk cleanup handler to update the disk cleanup manager on the progress of a scan for deletable files.

## -parameters

### -param dwlSpaceUsed [in]

Type: <b>DWORDLONG</b>

The amount of disk space that the handler can free at this point in the scan.

### -param dwFlags [in]

Type: <b>DWORD</b>

A flag that can be sent to the disk cleanup manager. This flag can have the following value. 



#### EVCCBF_LASTNOTIFICATION

This flag should be set if the handler will not call this method again. It is typically set when the scan is near completion.

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
The handler should continue scanning for deletable files.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
This value is returned when the user clicks the <b>Cancel</b> button on the disk cleanup manager's dialog box while a scan is in progress. The handler should stop scanning and shut down.

</td>
</tr>
</table>

## -remarks

This method is typically called by the handler's <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused">GetSpaceUsed</a> method while the handler is scanning for deletable files.