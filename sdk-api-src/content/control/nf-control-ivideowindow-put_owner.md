---
UID: NF:control.IVideoWindow.put_Owner
title: IVideoWindow::put_Owner (control.h)
author: windows-sdk-content
description: The put_Owner method specifies a parent window for the video window.
old-location: dshow\ivideowindow_put_owner.htm
tech.root: DirectShow
ms.assetid: 658ad234-cb5a-428b-ae19-0cd52db6718b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVideoWindow interface [DirectShow],put_Owner method, IVideoWindow.put_Owner, IVideoWindow::put_Owner, IVideoWindowput_Owner, control/IVideoWindow::put_Owner, dshow.ivideowindow_put_owner, put_Owner, put_Owner method [DirectShow], put_Owner method [DirectShow],IVideoWindow interface
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVideoWindow.put_Owner
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::put_Owner


## -description



The <code>put_Owner</code> method specifies a parent window for the video window.




## -parameters




### -param Owner [in]

A handle to the parent window, as an <a href="https://msdn.microsoft.com/80194b19-9c24-48f5-aca6-6ab33bd88c90">OAHWND</a> value, or <b>NULL</b> to remove the existing parent.
          


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



Use this method to display videos in a compound document. This method changes the parent of the video window and sets the WS_CHILD style for the video window.

Reset the owner to <b>NULL</b> before releasing the Filter Graph Manager. Otherwise, messages will continue to be sent to this window and errors will likely occur when the application is terminated.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377298(v=VS.85).aspx">IVideoWindow::get_Owner</a>
 

 

