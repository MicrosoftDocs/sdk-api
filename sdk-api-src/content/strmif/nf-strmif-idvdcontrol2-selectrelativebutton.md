---
UID: NF:strmif.IDvdControl2.SelectRelativeButton
title: IDvdControl2::SelectRelativeButton (strmif.h)
description: The SelectRelativeButton method sets the specified relative button (upper, lower, right, or left).helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","SelectRelativeButton method","IDvdControl2.SelectRelativeButton","IDvdControl2::SelectRelativeButton","IDvdControl2SelectRelativeButton","SelectRelativeButton","SelectRelativeButton method [DirectShow]","SelectRelativeButton method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_selectrelativebutton","strmif/IDvdControl2::SelectRelativeButton"]
old-location: dshow\idvdcontrol2_selectrelativebutton.htm
tech.root: DirectShow
ms.assetid: 2eb6243a-6f69-45d2-9b72-2dd28d02e86d
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],SelectRelativeButton method, IDvdControl2.SelectRelativeButton, IDvdControl2::SelectRelativeButton, IDvdControl2SelectRelativeButton, SelectRelativeButton, SelectRelativeButton method [DirectShow], SelectRelativeButton method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectrelativebutton, strmif/IDvdControl2::SelectRelativeButton
f1_keywords:
- strmif/IDvdControl2.SelectRelativeButton
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::SelectRelativeButton


## -description



The <code>SelectRelativeButton</code> method sets the specified relative button (upper, lower, right, or left).




## -parameters




### -param buttonDir


[DVD_RELATIVE_BUTTON](https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_relative_button) enumeration value indicating the button to select.


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
The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter is not in a valid domain.

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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/working-with-dvd-menus">Working With DVD Menus</a>
 

 

