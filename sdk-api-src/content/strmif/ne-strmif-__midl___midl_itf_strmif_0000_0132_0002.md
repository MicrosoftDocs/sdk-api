---
UID: NE:strmif.__MIDL___MIDL_itf_strmif_0000_0132_0002
title: "__MIDL___MIDL_itf_strmif_0000_0132_0002"
author: windows-sdk-content
description: Defines flags that control how the DVD Navigator Filter filter handles command synchronization.
old-location: dshow\dvd_cmd_flags.htm
tech.root: DirectShow
ms.assetid: 05eb5ab8-a1b3-4876-bac3-29510af8cdbd
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: DVD_CMD_FLAGS, DVD_CMD_FLAGS , DVD_CMD_FLAGS enumeration [DirectShow], DVD_CMD_FLAGSEnumeration, DVD_CMD_FLAG_Block, DVD_CMD_FLAG_EndAfterRendered, DVD_CMD_FLAG_Flush, DVD_CMD_FLAG_None, DVD_CMD_FLAG_SendEvents, DVD_CMD_FLAG_StartWhenRendered, __MIDL___MIDL_itf_strmif_0000_0132_0002, dshow.dvd_cmd_flags, strmif/DVD_CMD_FLAGS, strmif/DVD_CMD_FLAG_Block, strmif/DVD_CMD_FLAG_EndAfterRendered, strmif/DVD_CMD_FLAG_Flush, strmif/DVD_CMD_FLAG_None, strmif/DVD_CMD_FLAG_SendEvents, strmif/DVD_CMD_FLAG_StartWhenRendered
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_CMD_FLAGS
product: Windows
targetos: Windows
req.typenames: DVD_CMD_FLAGS
req.redist: 
---

# __MIDL___MIDL_itf_strmif_0000_0132_0002 enumeration


## -description



Defines flags that control how the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator Filter</a> filter handles command synchronization.




## -enum-fields




### -field DVD_CMD_FLAG_None

The DVD Navigator will not flush its buffers when it issues the command, will not send any events, and will not to block the thread of execution on any method call.


### -field DVD_CMD_FLAG_Flush

The DVD Navigator will flush all of its buffered video data before issuing the command. This can cause the DVD Navigator to discard approximately two seconds of video, which will decrease the response time but cause a gap in the playback data.


### -field DVD_CMD_FLAG_SendEvents

The DVD Navigator will send an <a href="https://msdn.microsoft.com/230116b4-23f1-4c37-a781-da2c5aa20a1f">EC_DVD_CMD_START</a> event when the command begins, and an <a href="https://msdn.microsoft.com/f460db8e-b966-41fa-bfa1-4ad3fa65c3e3">EC_DVD_CMD_END</a> event when the command ends. The event parameters contain the status code of the operation.


### -field DVD_CMD_FLAG_Block

The DVD Navigator blocks until the command completes or is canceled.


### -field DVD_CMD_FLAG_StartWhenRendered

Currently not used.


### -field DVD_CMD_FLAG_EndAfterRendered

The DVD Navigator will block until the specified action is actually rendered. This flag can be used with the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/fdf9642b-ac90-4ffc-a813-4a5b22a973dd">IDvdControl2::PlayChaptersAutoStop</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6c0d647c-a0c3-428e-8368-9204049dfea8">IDvdControl2::PlayPeriodInTitleAutoStop</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0553a0c4-34d3-4774-9a22-acc01c0a832a">IDvdControl2::SelectSubpictureStream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2e654bc1-293b-436b-bc33-8a8f269e9aee">IDvdControl2::SetSubpictureState</a>
</li>
</ul>
For example, when used with <a href="https://msdn.microsoft.com/fdf9642b-ac90-4ffc-a813-4a5b22a973dd">PlayChaptersAutoStop</a>, this flag causes the DVD Navigator to block until the specified chapters have all played. When used with <a href="https://msdn.microsoft.com/0553a0c4-34d3-4774-9a22-acc01c0a832a">SelectSubpictureStream</a>, the flag causes the DVD Navigator to block until the new subpicture is rendered.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/37e8f940-617d-43f6-92bd-aadccafe0059">Synchronizing DVD Commands</a>
 

 

