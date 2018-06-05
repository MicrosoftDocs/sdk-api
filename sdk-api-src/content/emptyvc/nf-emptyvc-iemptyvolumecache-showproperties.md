---
UID: NF:emptyvc.IEmptyVolumeCache.ShowProperties
title: IEmptyVolumeCache::ShowProperties
author: windows-sdk-content
description: Notifies the handler to display its UI.
old-location: lwef\iemptyvolumecache_showproperties.htm
old-project: lwef
ms.assetid: 3bce6251-b209-405a-8ac2-fd385f1c69ee
ms.author: windowssdkdev
ms.date: 04/27/2018
ms.keywords: IEmptyVolumeCache interface [Legacy Windows Environment Features],ShowProperties method, IEmptyVolumeCache.ShowProperties, IEmptyVolumeCache::ShowProperties, ShowProperties, ShowProperties method [Legacy Windows Environment Features], ShowProperties method [Legacy Windows Environment Features],IEmptyVolumeCache interface, _win32_IEmptyVolumeCache_ShowProperties, emptyvc/IEmptyVolumeCache::ShowProperties, lwef.iemptyvolumecache_showproperties, shell.iemptyvolumecache_showproperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: EMI_VERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IEmptyVolumeCache.ShowProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Windows Media Format 9 Series or later
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



A handler can display a UI, which is typically used to allow the user to select which files are to be cleaned up and how. To do so, the handler sets the <b>EVCF_HASSETTINGS</b> flag in the <i>pdwFlags</i> parameter when <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> is called. The disk cleanup manager will then display a <b>Settings</b> button. When that button is clicked, the disk cleanup manager calls <b>ShowProperties</b> to notify the handler to display its UI.



