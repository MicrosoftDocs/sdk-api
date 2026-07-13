---
UID: NF:wtsapi32.WTSVirtualChannelOpenEx
title: WTSVirtualChannelOpenEx function (wtsapi32.h)
description: Creates a virtual channel in a manner similar to WTSVirtualChannelOpen.
helpviewer_keywords: ["WTSVirtualChannelOpenEx","WTSVirtualChannelOpenEx function [Remote Desktop Services]","WTS_CHANNEL_OPTION_DYNAMIC_NO_COMPRESS","WTS_CHANNEL_OPTION_DYNAMIC_PRI_HIGH","WTS_CHANNEL_OPTION_DYNAMIC_PRI_LOW (default)","WTS_CHANNEL_OPTION_DYNAMIC_PRI_MED","WTS_CHANNEL_OPTION_DYNAMIC_PRI_REAL","termserv.wtsvirtualchannelopenex","wtsapi32/WTSVirtualChannelOpenEx"]
old-location: termserv\wtsvirtualchannelopenex.htm
tech.root: TermServ
ms.assetid: 5694c4b6-3d0f-4a48-8d15-1e404cbb6164
ms.date: 12/05/2018
ms.keywords: WTSVirtualChannelOpenEx, WTSVirtualChannelOpenEx function [Remote Desktop Services], WTS_CHANNEL_OPTION_DYNAMIC_NO_COMPRESS, WTS_CHANNEL_OPTION_DYNAMIC_PRI_HIGH, WTS_CHANNEL_OPTION_DYNAMIC_PRI_LOW (default), WTS_CHANNEL_OPTION_DYNAMIC_PRI_MED, WTS_CHANNEL_OPTION_DYNAMIC_PRI_REAL, termserv.wtsvirtualchannelopenex, wtsapi32/WTSVirtualChannelOpenEx
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSVirtualChannelOpenEx
 - wtsapi32/WTSVirtualChannelOpenEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-session-wtsapi32-l1-1-1.dll
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSVirtualChannelOpenEx
req.apiset: ext-ms-win-session-wtsapi32-l1-1-0 (introduced in Windows 8)
---

# WTSVirtualChannelOpenEx function


## -description

Creates a virtual channel in a manner similar to 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelopen">WTSVirtualChannelOpen</a>.

This API supports both static virtual channel (SVC) and dynamic virtual channel (DVC) creation. If the 
    <i>flags</i> parameter is zero, it behaves the same as 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelopen">WTSVirtualChannelOpen</a>. A DVC can be opened 
    by specifying the appropriate flag. After a DVC is created, you can use the same functions for Read, Write, Query, 
    or Close that are used for the SVC.

## -parameters

### -param SessionId [in]

A Remote Desktop Services session identifier. To indicate the current session, specify 
       <b>WTS_CURRENT_SESSION</b>. You can use the 
       <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa">WTSEnumerateSessions</a> function to retrieve 
       the identifiers of all sessions on a specified RD Session Host server.

To be able to open a virtual channel on another user's session, you must have the Virtual Channels 
       permission. For more information, see 
       <a href="/windows/desktop/TermServ/terminal-services-permissions">Remote Desktop Services Permissions</a>. 
       To modify permissions on a session, use the Remote Desktop Services Configuration administrative tool.

### -param pVirtualName [in]

In the case of an SVC, points to a null-terminated string that contains the virtual channel name. The length 
       of an SVC name is limited to <b>CHANNEL_NAME_LEN</b> characters, not including the 
       terminating null.

In the case of a DVC, points to a null-terminated string that contains the endpoint name of the listener. The 
       length of a DVC name is limited to <b>MAX_PATH</b> characters.

### -param flags [in]

To open the channel as an SVC, specify zero for this parameter. To open the channel as a DVC, specify 
       <b>WTS_CHANNEL_OPTION_DYNAMIC</b>.

When opening a DVC, you can specify a priority setting for the data that is being transferred by specifying 
       one of the <b>WTS_CHANNEL_OPTION_DYNAMIC_PRI_<i>XXX</i></b> values in 
       combination with the <b>WTS_CHANNEL_OPTION_DYNAMIC</b> value.



#### WTS_CHANNEL_OPTION_DYNAMIC_NO_COMPRESS

Disables compression for this DVC. You must specify this value in combination with the 
        <b>WTS_CHANNEL_OPTION_DYNAMIC</b> value.



#### WTS_CHANNEL_OPTION_DYNAMIC_PRI_LOW (default)

Low priority. The data will be sent on both sides with low priority. Use this priority level for block 
        transfers of all sizes, where the transfer speed is not important. In almost all (95%) cases, the channel 
        should be opened with this flag.



#### WTS_CHANNEL_OPTION_DYNAMIC_PRI_MED

Medium priority. Use this priority level to send short control messages that must have priority over the 
        data in the low priority channels.



#### WTS_CHANNEL_OPTION_DYNAMIC_PRI_HIGH

High priority. Use this priority level for data that is critical and directly affects the user 
        experience. The transfer size may vary. Display data falls into this category.



#### WTS_CHANNEL_OPTION_DYNAMIC_PRI_REAL

Real-time priority. Use this priority level only in cases where the data transfer is absolutely critical. 
        The data transfer size should be limited to a few hundred bytes per message.

## -returns

<b>NULL</b> on error with 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> set.

## -see-also

<a href="/windows/desktop/TermServ/dvc-server-apis">DVC Server APIs</a>



<a href="/windows/desktop/TermServ/dynamic-virtual-channels-reference">Dynamic Virtual Channels Reference</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelopen">WTSVirtualChannelOpen</a>
