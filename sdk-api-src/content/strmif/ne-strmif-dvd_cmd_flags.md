---
UID: NE:strmif.__MIDL___MIDL_itf_strmif_0000_0132_0002
title: DVD_CMD_FLAGS (strmif.h)
description: Defines flags that control how the DVD Navigator Filter filter handles command synchronization.
helpviewer_keywords: ["DVD_CMD_FLAGS","DVD_CMD_FLAGS","DVD_CMD_FLAGS enumeration [DirectShow]","DVD_CMD_FLAGSEnumeration","DVD_CMD_FLAG_Block","DVD_CMD_FLAG_EndAfterRendered","DVD_CMD_FLAG_Flush","DVD_CMD_FLAG_None","DVD_CMD_FLAG_SendEvents","DVD_CMD_FLAG_StartWhenRendered","dshow.dvd_cmd_flags","strmif/DVD_CMD_FLAGS","strmif/DVD_CMD_FLAG_Block","strmif/DVD_CMD_FLAG_EndAfterRendered","strmif/DVD_CMD_FLAG_Flush","strmif/DVD_CMD_FLAG_None","strmif/DVD_CMD_FLAG_SendEvents","strmif/DVD_CMD_FLAG_StartWhenRendered"]
old-location: dshow\dvd_cmd_flags.htm
tech.root: dshow
ms.assetid: 05eb5ab8-a1b3-4876-bac3-29510af8cdbd
ms.date: 12/05/2018
ms.keywords: DVD_CMD_FLAGS, DVD_CMD_FLAGS , DVD_CMD_FLAGS enumeration [DirectShow], DVD_CMD_FLAGSEnumeration, DVD_CMD_FLAG_Block, DVD_CMD_FLAG_EndAfterRendered, DVD_CMD_FLAG_Flush, DVD_CMD_FLAG_None, DVD_CMD_FLAG_SendEvents, DVD_CMD_FLAG_StartWhenRendered, dshow.dvd_cmd_flags, strmif/DVD_CMD_FLAGS, strmif/DVD_CMD_FLAG_Block, strmif/DVD_CMD_FLAG_EndAfterRendered, strmif/DVD_CMD_FLAG_Flush, strmif/DVD_CMD_FLAG_None, strmif/DVD_CMD_FLAG_SendEvents, strmif/DVD_CMD_FLAG_StartWhenRendered
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DVD_CMD_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_strmif_0000_0132_0002
 - strmif/__MIDL___MIDL_itf_strmif_0000_0132_0002
 - DVD_CMD_FLAGS
 - strmif/DVD_CMD_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_CMD_FLAGS
---

# DVD_CMD_FLAGS enumeration


## -description

Defines flags that control how the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator Filter</a> filter handles command synchronization.

## -enum-fields

### -field DVD_CMD_FLAG_None:0

The DVD Navigator will not flush its buffers when it issues the command, will not send any events, and will not to block the thread of execution on any method call.

### -field DVD_CMD_FLAG_Flush:0x1

The DVD Navigator will flush all of its buffered video data before issuing the command. This can cause the DVD Navigator to discard approximately two seconds of video, which will decrease the response time but cause a gap in the playback data.

### -field DVD_CMD_FLAG_SendEvents:0x2

The DVD Navigator will send an <a href="/windows/desktop/DirectShow/ec-dvd-cmd-start">EC_DVD_CMD_START</a> event when the command begins, and an <a href="/windows/desktop/DirectShow/ec-dvd-cmd-end">EC_DVD_CMD_END</a> event when the command ends. The event parameters contain the status code of the operation.

### -field DVD_CMD_FLAG_Block:0x4

The DVD Navigator blocks until the command completes or is canceled.

### -field DVD_CMD_FLAG_StartWhenRendered:0x8

Currently not used.

### -field DVD_CMD_FLAG_EndAfterRendered:0x10

The DVD Navigator will block until the specified action is actually rendered. This flag can be used with the following methods:

<ul>
<li>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playchaptersautostop">IDvdControl2::PlayChaptersAutoStop</a>
</li>
<li>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop">IDvdControl2::PlayPeriodInTitleAutoStop</a>
</li>
<li>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectsubpicturestream">IDvdControl2::SelectSubpictureStream</a>
</li>
<li>
<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setsubpicturestate">IDvdControl2::SetSubpictureState</a>
</li>
</ul>
For example, when used with <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playchaptersautostop">PlayChaptersAutoStop</a>, this flag causes the DVD Navigator to block until the specified chapters have all played. When used with <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectsubpicturestream">SelectSubpictureStream</a>, the flag causes the DVD Navigator to block until the new subpicture is rendered.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>
