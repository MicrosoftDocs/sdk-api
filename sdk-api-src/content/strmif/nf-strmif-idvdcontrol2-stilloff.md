---
UID: NF:strmif.IDvdControl2.StillOff
title: IDvdControl2::StillOff (strmif.h)
description: The StillOff method resumes playback, canceling still mode.helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","StillOff method","IDvdControl2.StillOff","IDvdControl2::StillOff","IDvdControl2StillOff","StillOff","StillOff method [DirectShow]","StillOff method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_stilloff","strmif/IDvdControl2::StillOff"]
old-location: dshow\idvdcontrol2_stilloff.htm
tech.root: DirectShow
ms.assetid: 6c419a3b-482a-4b1b-afea-6cbf9373c5b9
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],StillOff method, IDvdControl2.StillOff, IDvdControl2::StillOff, IDvdControl2StillOff, StillOff, StillOff method [DirectShow], StillOff method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_stilloff, strmif/IDvdControl2::StillOff
f1_keywords:
- strmif/IDvdControl2.StillOff
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
- IDvdControl2.StillOff
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::StillOff


## -description



The <code>StillOff</code> method resumes playback, canceling still mode.




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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter is in a menu domain and the menu has buttons.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Invalid domain.

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



A <i>still</i> is a static image presented by the disc. It is not the same as the frozen display image that appears when the user clicks the <b>Pause</b> button. When the DVD Navigator encounters a still image, it sends the application an EC_DVD_STILL_ON message, goes into still-store mode displaying the image, and waits for <code>StillOff</code> to be called before resuming playback.

If the DVD Navigator is not in still-store mode, this method does nothing.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Still_Off</td>
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
 

 

