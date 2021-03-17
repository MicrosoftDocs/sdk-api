---
UID: NF:emptyvc.IEmptyVolumeCache.ShowProperties
title: IEmptyVolumeCache::ShowProperties (emptyvc.h)
description: Notifies the handler to display its UI.
helpviewer_keywords: ["IEmptyVolumeCache interface [Legacy Windows Environment Features]","ShowProperties method","IEmptyVolumeCache.ShowProperties","IEmptyVolumeCache::ShowProperties","ShowProperties","ShowProperties method [Legacy Windows Environment Features]","ShowProperties method [Legacy Windows Environment Features]","IEmptyVolumeCache interface","_win32_IEmptyVolumeCache_ShowProperties","emptyvc/IEmptyVolumeCache::ShowProperties","lwef.iemptyvolumecache_showproperties","shell.iemptyvolumecache_showproperties"]
old-location: lwef\iemptyvolumecache_showproperties.htm
tech.root: lwef
ms.assetid: 3bce6251-b209-405a-8ac2-fd385f1c69ee
ms.date: 12/05/2018
ms.keywords: IEmptyVolumeCache interface [Legacy Windows Environment Features],ShowProperties method, IEmptyVolumeCache.ShowProperties, IEmptyVolumeCache::ShowProperties, ShowProperties, ShowProperties method [Legacy Windows Environment Features], ShowProperties method [Legacy Windows Environment Features],IEmptyVolumeCache interface, _win32_IEmptyVolumeCache_ShowProperties, emptyvc/IEmptyVolumeCache::ShowProperties, lwef.iemptyvolumecache_showproperties, shell.iemptyvolumecache_showproperties
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
 - IEmptyVolumeCache::ShowProperties
 - emptyvc/IEmptyVolumeCache::ShowProperties
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
 - IEmptyVolumeCache.ShowProperties
---

# IEmptyVolumeCache::ShowProperties


## -description

Notifies the handler to display its UI.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The parent window to be used when displaying the UI.

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
The user changed one or more settings.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No settings were changed.

</td>
</tr>
</table>

## -remarks

A handler can display a UI, which is typically used to allow the user to select which files are to be cleaned up and how. To do so, the handler sets the <b>EVCF_HASSETTINGS</b> flag in the <i>pdwFlags</i> parameter when <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-initialize">Initialize</a> is called. The disk cleanup manager will then display a <b>Settings</b> button. When that button is clicked, the disk cleanup manager calls <b>ShowProperties</b> to notify the handler to display its UI.