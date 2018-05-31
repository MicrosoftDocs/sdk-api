---
UID: NF:control.IVideoWindow.SetWindowPosition
title: IVideoWindow::SetWindowPosition
author: windows-sdk-content
description: The SetWindowPosition method sets the position of the video window.
old-location: dshow\ivideowindow_setwindowposition.htm
old-project: DirectShow
ms.assetid: 5e667044-1781-4380-b855-d15cf8cd2349
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IVideoWindow interface [DirectShow],SetWindowPosition method, IVideoWindow.SetWindowPosition, IVideoWindow::SetWindowPosition, IVideoWindowSetWindowPosition, SetWindowPosition, SetWindowPosition method [DirectShow], SetWindowPosition method [DirectShow],IVideoWindow interface, control/IVideoWindow::SetWindowPosition, dshow.ivideowindow_setwindowposition
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
-	IVideoWindow.SetWindowPosition
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::SetWindowPosition


## -description



The <code>SetWindowPosition</code> method sets the position of the video window.




## -parameters




### -param Left [in]


            The x-coordinate, in pixels.
          


### -param Top [in]


            The y-coordinate, in pixels.
          


### -param Width [in]

The width, in pixels.
          


### -param Height [in]

The height, in pixels.
          


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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



This method has the same effect as calling the <a href="https://msdn.microsoft.com/a614ee46-49cf-40e4-a1f7-b3b3b7065175">IVideoWindow::put_Left</a>, <a href="https://msdn.microsoft.com/1a5df1f1-3867-4956-8e1b-090aa8d8ff3a">IVideoWindow::put_Top</a>, <a href="https://msdn.microsoft.com/7cb02033-0405-4b8b-91fc-2f33097f2c88">IVideoWindow::put_Width</a>, and <a href="https://msdn.microsoft.com/39ba411f-675f-4dad-be4f-6beffbd3b53c">IVideoWindow::put_Height</a> methods.

If resizing the window to the specified dimensions is impossible, this method modifies the window's size and location to make the window fit. Call the <a href="https://msdn.microsoft.com/df55c10d-aec1-42f3-8bfb-207ae8804e72">IVideoWindow::GetWindowPosition</a> method to determine the result.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>
 

 

