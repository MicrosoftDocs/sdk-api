---
UID: NF:control.IVideoWindow.GetRestorePosition
title: IVideoWindow::GetRestorePosition
author: windows-sdk-content
description: The GetRestorePosition method retrieves the restored window position.
old-location: dshow\ivideowindow_getrestoreposition.htm
old-project: DirectShow
ms.assetid: e2c8880a-e140-4bb1-8f0d-2d665c98728c
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetRestorePosition, GetRestorePosition method [DirectShow], GetRestorePosition method [DirectShow],IVideoWindow interface, IVideoWindow interface [DirectShow],GetRestorePosition method, IVideoWindow.GetRestorePosition, IVideoWindow::GetRestorePosition, IVideoWindowGetRestorePosition, control/IVideoWindow::GetRestorePosition, dshow.ivideowindow_getrestoreposition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WMPContextMenuInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVideoWindow.GetRestorePosition
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::GetRestorePosition


## -description



The <code>GetRestorePosition</code> method retrieves the restored window position.




## -parameters




### -param pLeft [out]


            Receives the x-coordinate, in pixels.
          


### -param pTop [out]

Receives the y-coordinate, in pixels.
          


### -param pWidth [out]

Receives the width of the window, in pixels.
          


### -param pHeight [out]

Receives the height of the window, in pixels.
          


## -returns



Possible return values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer.

</td>
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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The video renderer filter is not connected.

</td>
</tr>
</table>
 




## -remarks



If the video window is minimized or maximized, you can use this method to get the window's restored position.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>
 

 

