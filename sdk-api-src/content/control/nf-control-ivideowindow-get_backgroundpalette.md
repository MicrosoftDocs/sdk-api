---
UID: NF:control.IVideoWindow.get_BackgroundPalette
title: IVideoWindow::get_BackgroundPalette
author: windows-sdk-content
description: The get_BackgroundPalette method queries whether the video window realizes its palette in the background..
old-location: dshow\ivideowindow_get_backgroundpalette.htm
old-project: DirectShow
ms.assetid: cdd11f60-e042-4aad-a867-d1e12a88ebfe
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IVideoWindow interface [DirectShow],get_BackgroundPalette method, IVideoWindow.get_BackgroundPalette, IVideoWindow::get_BackgroundPalette, IVideoWindowget_BackgroundPalette, control/IVideoWindow::get_BackgroundPalette, dshow.ivideowindow_get_backgroundpalette, get_BackgroundPalette, get_BackgroundPalette method [DirectShow], get_BackgroundPalette method [DirectShow],IVideoWindow interface
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVideoWindow.get_BackgroundPalette
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::get_BackgroundPalette


## -description



The <code>get_BackgroundPalette</code> method queries whether the video window realizes its palette in the background..




## -parameters




### -param pBackgroundPalette [out]

Receives one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>
                  OATRUE
                </td>
<td>The video window realizes the palette in the background.</td>
</tr>
<tr>
<td>
                  OAFALSE
                </td>
<td>The video window does not realize the palette in the background.</td>
</tr>
</table>
 


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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/0b1d34b6-0043-4929-a496-cf84b5d47b55">IVideoWindow::put_BackgroundPalette</a>
 

 

