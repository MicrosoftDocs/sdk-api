---
UID: NF:strmif.IDvdControl2.SelectAtPosition
title: IDvdControl2::SelectAtPosition
author: windows-sdk-content
description: The SelectAtPosition method highlights the menu button under the mouse pointer position.
old-location: dshow\idvdcontrol2_selectatposition.htm
tech.root: DirectShow
ms.assetid: f6cb9cb4-0792-43f5-b53b-02a38ccf0398
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDvdControl2 interface [DirectShow],SelectAtPosition method, IDvdControl2.SelectAtPosition, IDvdControl2::SelectAtPosition, IDvdControl2SelectAtPosition, SelectAtPosition, SelectAtPosition method [DirectShow], SelectAtPosition method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectatposition, strmif/IDvdControl2::SelectAtPosition
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDvdControl2.SelectAtPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl2::SelectAtPosition


## -description



The <code>SelectAtPosition</code> method highlights the menu button under the mouse pointer position.




## -parameters




### -param point [in]

Point on the screen, in screen pixel coordinates.


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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NO_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
No button is present at the mouse pointer position.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The DVD Navigator is in the Stop domain.

</td>
</tr>
</table>
 




## -remarks



Note that angle and menu button indexes are one-based while audio stream and subpicture stream indexes are zero-based.

Call <a href="https://msdn.microsoft.com/20213874-ed28-4e0a-83af-044570b2c7e3">IDvdControl2::ActivateButton</a> in response to a mouse click when the pointer is over a menu button.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

This method is demonstrated in the DVDSample application in <b>CDvdCore::OnMouseEvent</b>.

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
<li>DVD_DOMAIN_Title</li>
<li>DVD_DOMAIN_FirstPlay</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>



<a href="https://msdn.microsoft.com/8c5f8072-b74f-4e15-8991-73bcc4145fd2">Working With DVD Menus</a>
 

 

