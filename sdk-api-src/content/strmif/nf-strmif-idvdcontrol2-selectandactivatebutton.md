---
UID: NF:strmif.IDvdControl2.SelectAndActivateButton
title: IDvdControl2::SelectAndActivateButton (strmif.h)
description: The SelectAndActivateButton method selects and activates the specified menu button.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","SelectAndActivateButton method","IDvdControl2.SelectAndActivateButton","IDvdControl2::SelectAndActivateButton","IDvdControl2SelectAndActivateButton","SelectAndActivateButton","SelectAndActivateButton method [DirectShow]","SelectAndActivateButton method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_selectandactivatebutton","strmif/IDvdControl2::SelectAndActivateButton"]
old-location: dshow\idvdcontrol2_selectandactivatebutton.htm
tech.root: dshow
ms.assetid: 1e5ad753-bc35-4a98-83d8-82ffccbbe3ed
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],SelectAndActivateButton method, IDvdControl2.SelectAndActivateButton, IDvdControl2::SelectAndActivateButton, IDvdControl2SelectAndActivateButton, SelectAndActivateButton, SelectAndActivateButton method [DirectShow], SelectAndActivateButton method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectandactivatebutton, strmif/IDvdControl2::SelectAndActivateButton
f1_keywords:
- strmif/IDvdControl2.SelectAndActivateButton
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
- IDvdControl2.SelectAndActivateButton
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::SelectAndActivateButton


## -description



The <code>SelectAndActivateButton</code> method selects and activates the specified menu button.




## -parameters




### -param ulButton [in]

Value from 1 through 36 that specifies the button to select and activate.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ulButton</i> is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>ulButton</i> value is valid, but the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter couldn't activate it.

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
<td>Button_Select_and_Activate</td>
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
 

 

