---
UID: NF:strmif.IDvdControl2.ReturnFromSubmenu
title: IDvdControl2::ReturnFromSubmenu (strmif.h)
description: The ReturnFromSubmenu method returns the display from a submenu to its parent menu.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","ReturnFromSubmenu method","IDvdControl2.ReturnFromSubmenu","IDvdControl2::ReturnFromSubmenu","IDvdControl2ReturnFromSubmenu","ReturnFromSubmenu","ReturnFromSubmenu method [DirectShow]","ReturnFromSubmenu method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_returnfromsubmenu","strmif/IDvdControl2::ReturnFromSubmenu"]
old-location: dshow\idvdcontrol2_returnfromsubmenu.htm
tech.root: dshow
ms.assetid: ef213ab6-3993-46e4-803d-3ce195256e7e
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],ReturnFromSubmenu method, IDvdControl2.ReturnFromSubmenu, IDvdControl2::ReturnFromSubmenu, IDvdControl2ReturnFromSubmenu, ReturnFromSubmenu, ReturnFromSubmenu method [DirectShow], ReturnFromSubmenu method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_returnfromsubmenu, strmif/IDvdControl2::ReturnFromSubmenu
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdControl2::ReturnFromSubmenu
 - strmif/IDvdControl2::ReturnFromSubmenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdControl2.ReturnFromSubmenu
---

# IDvdControl2::ReturnFromSubmenu


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ReturnFromSubmenu</code> method returns the display from a submenu to its parent menu.

## -parameters

### -param dwFlags [in]

Bitwise OR of one or more flags from the <a href="/windows/desktop/api/strmif/ne-strmif-dvd_cmd_flags">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.

### -param ppCmd [out]

Receives a pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>.

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
<dt><b>VFW_E_DVD_NO_GOUP_PGC</b></dt>
</dl>
</td>
<td width="60%">
The operation cannot be performed because no GoUp program chain (PGC) is available.

</td>
</tr>
</table>

## -remarks

If the DVD Navigator is at the top-level menu, this method calls the <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-resume">IDvdControl2::Resume</a> method so that play continues where it left off.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>GoUP</td>
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

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>



<a href="/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>



<a href="/windows/desktop/DirectShow/working-with-dvd-menus">Working With DVD Menus</a>