---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# WTSVirtualChannelOpenEx function


## -description


Creates a virtual channel in a manner similar to 
    <a href="https://msdn.microsoft.com/0daaf06f-ba05-469c-b888-3df5d9495364">WTSVirtualChannelOpen</a>.

This API supports both static virtual channel (SVC) and dynamic virtual channel (DVC) creation. If the 
    <i>flags</i> parameter is zero, it behaves the same as 
    <a href="https://msdn.microsoft.com/0daaf06f-ba05-469c-b888-3df5d9495364">WTSVirtualChannelOpen</a>. A DVC can be opened 
    by specifying the appropriate flag. After a DVC is created, you can use the same functions for Read, Write, Query, 
    or Close that are used for the SVC.


## -parameters




### -param SessionId [in]

A Remote Desktop Services session identifier. To indicate the current session, specify 
       <b>WTS_CURRENT_SESSION</b>. You can use the 
       <a href="https://msdn.microsoft.com/6f9dd7d4-48dc-411c-85f1-cd1239d1e106">WTSEnumerateSessions</a> function to retrieve 
       the identifiers of all sessions on a specified RD Session Host server.

To be able to open a virtual channel on another user's session, you must have the Virtual Channels 
       permission. For more information, see 
       <a href="https://msdn.microsoft.com/448a7f9b-bf12-48eb-a3e7-4512ec288d95">Remote Desktop Services Permissions</a>. 
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
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> set.




## -see-also




<a href="https://msdn.microsoft.com/9743ce32-9262-4af3-b013-668e834e279c">DVC Server APIs</a>



<a href="https://msdn.microsoft.com/00cb7813-1d86-4faa-8b46-081959e4acfa">Dynamic Virtual Channels Reference</a>



<a href="https://msdn.microsoft.com/0daaf06f-ba05-469c-b888-3df5d9495364">WTSVirtualChannelOpen</a>
 

 

