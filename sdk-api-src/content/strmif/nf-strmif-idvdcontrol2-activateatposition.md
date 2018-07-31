---
UID: NF:strmif.IDvdControl2.ActivateAtPosition
title: IDvdControl2::ActivateAtPosition
author: windows-sdk-content
description: The ActivateAtPosition method activates the menu button under the mouse pointer position.
old-location: dshow\idvdcontrol2_activateatposition.htm
old-project: DirectShow
ms.assetid: ff9eb02c-09c0-4b58-8e38-ec84ab1f1c42
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ActivateAtPosition, ActivateAtPosition method [DirectShow], ActivateAtPosition method [DirectShow],IDvdControl2 interface, IDvdControl2 interface [DirectShow],ActivateAtPosition method, IDvdControl2.ActivateAtPosition, IDvdControl2::ActivateAtPosition, IDvdControl2ActivateAtPosition, dshow.idvdcontrol2_activateatposition, strmif/IDvdControl2::ActivateAtPosition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdControl2.ActivateAtPosition
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl2::ActivateAtPosition


## -description



The <code>ActivateAtPosition</code> method activates the menu button under the mouse pointer position.




## -parameters




### -param point [in]

Point on the client window area, in screen pixel coordinates.


## -returns



Returns one of the following values.

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
The click occurred in the highlighted button rectangle, and the button was successfully activated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The point lies outside the valid video region.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The button is present but is not working.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The DVD Navigator is not in a menu domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NO_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
There is no menu button under the mouse pointer position.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
The operation is inhibited by user operation (UOP) control.

</td>
</tr>
</table>
 




## -remarks



The mouse pointer coordinates are relative to the upper left of the client area, which isn't necessarily the video display area if the video is in letterbox format.

Use this method when the user is navigating through a menu by moving the mouse pointer directly over the menu buttons. If the user is using the relative buttons to navigate the menu, use <a href="https://msdn.microsoft.com/20213874-ed28-4e0a-83af-044570b2c7e3">ActivateButton</a> rather than <code>ActivateAtPosition</code>.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>None</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>



<a href="https://msdn.microsoft.com/8c5f8072-b74f-4e15-8991-73bcc4145fd2">Working With DVD Menus</a>
 

 

