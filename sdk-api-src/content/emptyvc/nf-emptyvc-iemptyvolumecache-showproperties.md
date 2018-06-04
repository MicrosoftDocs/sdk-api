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



