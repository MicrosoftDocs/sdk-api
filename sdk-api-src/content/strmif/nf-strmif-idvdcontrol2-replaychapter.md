---
UID: NF:strmif.IDvdControl2.ReplayChapter
title: IDvdControl2::ReplayChapter (strmif.h)
description: The ReplayChapter method starts playback from the beginning of the current chapter.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","ReplayChapter method","IDvdControl2.ReplayChapter","IDvdControl2::ReplayChapter","IDvdControl2ReplayChapter","ReplayChapter","ReplayChapter method [DirectShow]","ReplayChapter method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_replaychapter","strmif/IDvdControl2::ReplayChapter"]
old-location: dshow\idvdcontrol2_replaychapter.htm
tech.root: dshow
ms.assetid: ea1567fc-708f-4dcd-abc2-b5bdc9f6a62c
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],ReplayChapter method, IDvdControl2.ReplayChapter, IDvdControl2::ReplayChapter, IDvdControl2ReplayChapter, ReplayChapter, ReplayChapter method [DirectShow], ReplayChapter method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_replaychapter, strmif/IDvdControl2::ReplayChapter
f1_keywords:
- strmif/IDvdControl2.ReplayChapter
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
- IDvdControl2.ReplayChapter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::ReplayChapter


## -description



The <code>ReplayChapter</code> method starts playback from the beginning of the current chapter.




## -parameters




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
<td>TopPG_Search</td>
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



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>
 

 

