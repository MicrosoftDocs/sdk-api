---
UID: NF:strmif.IDvdControl2.SelectRelativeButton
title: IDvdControl2::SelectRelativeButton (strmif.h)
author: windows-sdk-content
description: The SelectRelativeButton method sets the specified relative button (upper, lower, right, or left).
old-location: dshow\idvdcontrol2_selectrelativebutton.htm
tech.root: DirectShow
ms.assetid: 2eb6243a-6f69-45d2-9b72-2dd28d02e86d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],SelectRelativeButton method, IDvdControl2.SelectRelativeButton, IDvdControl2::SelectRelativeButton, IDvdControl2SelectRelativeButton, SelectRelativeButton, SelectRelativeButton method [DirectShow], SelectRelativeButton method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectrelativebutton, strmif/IDvdControl2::SelectRelativeButton
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
 - IDvdControl2.SelectRelativeButton
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl2::SelectRelativeButton


## -description



The <code>SelectRelativeButton</code> method sets the specified relative button (upper, lower, right, or left).




## -parameters




### -param buttonDir


<a href="https://msdn.microsoft.com/f2641b5c-08a4-44a1-8f53-fad636a03c45">DVD_RELATIVE_BUTTON</a> enumeration value indicating the button to select.


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
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter is not in a valid domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
</tr>
</table>
 




## -remarks



The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>(Left/Right/Upper/Lower)_Button_Select</td>
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
 

 

