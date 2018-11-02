---
UID: NF:strmif.IDvdControl2.ActivateButton
title: IDvdControl2::ActivateButton
author: windows-sdk-content
description: The ActivateButton method activates the currently selected menu button.
old-location: dshow\idvdcontrol2_activatebutton.htm
tech.root: DirectShow
ms.assetid: 20213874-ed28-4e0a-83af-044570b2c7e3
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ActivateButton, ActivateButton method [DirectShow], ActivateButton method [DirectShow],IDvdControl2 interface, IDvdControl2 interface [DirectShow],ActivateButton method, IDvdControl2.ActivateButton, IDvdControl2::ActivateButton, IDvdControl2ActivateButton, dshow.idvdcontrol2_activatebutton, strmif/IDvdControl2::ActivateButton
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
 - IDvdControl2.ActivateButton
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl2::ActivateButton


## -description



The <code>ActivateButton</code> method activates the currently selected menu button.




## -parameters






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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The DVD Navigator is in an invalid domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the DVD Navigator from entering a paused state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NO_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
No button is selected.

</td>
</tr>
</table>
 




## -remarks



An application might or might not have four relative buttons on the side of the video display to represent the buttons on a physical remote control. These enable a user to select menu buttons but not activate them. A fifth button is required to activate the selected button. Call <code>ActivateButton</code> in response to a mouse click on the fifth button.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Button_Activate</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Title</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>



<a href="https://msdn.microsoft.com/8c5f8072-b74f-4e15-8991-73bcc4145fd2">Working With DVD Menus</a>
 

 

