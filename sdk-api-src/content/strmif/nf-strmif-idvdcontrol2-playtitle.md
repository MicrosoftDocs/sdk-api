---
UID: NF:strmif.IDvdControl2.PlayTitle
title: IDvdControl2::PlayTitle (strmif.h)
description: The PlayTitle method starts playback from the beginning of the specified title.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","PlayTitle method","IDvdControl2.PlayTitle","IDvdControl2::PlayTitle","IDvdControl2PlayTitle","PlayTitle","PlayTitle method [DirectShow]","PlayTitle method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_playtitle","strmif/IDvdControl2::PlayTitle"]
old-location: dshow\idvdcontrol2_playtitle.htm
tech.root: dshow
ms.assetid: 5cdea69e-7d32-470e-846b-1b2be5ca87b1
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],PlayTitle method, IDvdControl2.PlayTitle, IDvdControl2::PlayTitle, IDvdControl2PlayTitle, PlayTitle, PlayTitle method [DirectShow], PlayTitle method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_playtitle, strmif/IDvdControl2::PlayTitle
f1_keywords:
- strmif/IDvdControl2.PlayTitle
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
- IDvdControl2.PlayTitle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::PlayTitle


## -description



The <code>PlayTitle</code> method starts playback from the beginning of the specified title.




## -parameters




### -param ulTitle

Value that specifies the title number; this value must be from 1 through 99.


### -param dwFlags [in]

Bitwise OR of one or more flags from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_cmd_flags">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.


### -param ppCmd [out]

Receives a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>.


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
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
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
<td>Title_Play</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Title</li>
<li>DVD_DOMAIN_Stop</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>
 

 

