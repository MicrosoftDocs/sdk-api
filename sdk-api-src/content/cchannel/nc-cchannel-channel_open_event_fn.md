---
UID: NC:cchannel.CHANNEL_OPEN_EVENT_FN
title: CHANNEL_OPEN_EVENT_FN (cchannel.h)
description: An application-defined callback function that Remote Desktop Services calls to notify the client DLL of events for a specific virtual channel.
helpviewer_keywords: ["CHANNEL_EVENT_DATA_RECEIVED","CHANNEL_EVENT_WRITE_CANCELLED","CHANNEL_EVENT_WRITE_COMPLETE","CHANNEL_FLAG_FIRST","CHANNEL_FLAG_LAST","CHANNEL_FLAG_MIDDLE","CHANNEL_FLAG_ONLY","CHANNEL_OPEN_EVENT_FN","CHANNEL_OPEN_EVENT_FN callback function [Remote Desktop Services]","VirtualChannelOpenEvent callback","_win32_virtualchannelopenevent","cchannel/CHANNEL_OPEN_EVENT_FN","termserv.virtualchannelopenevent"]
old-location: termserv\virtualchannelopenevent.htm
tech.root: TermServ
ms.assetid: 7412d125-1a3c-4e9a-9804-b612030682da
ms.date: 12/05/2018
ms.keywords: CHANNEL_EVENT_DATA_RECEIVED, CHANNEL_EVENT_WRITE_CANCELLED, CHANNEL_EVENT_WRITE_COMPLETE, CHANNEL_FLAG_FIRST, CHANNEL_FLAG_LAST, CHANNEL_FLAG_MIDDLE, CHANNEL_FLAG_ONLY, CHANNEL_OPEN_EVENT_FN, CHANNEL_OPEN_EVENT_FN callback function [Remote Desktop Services], VirtualChannelOpenEvent callback, _win32_virtualchannelopenevent, cchannel/CHANNEL_OPEN_EVENT_FN, termserv.virtualchannelopenevent
req.header: cchannel.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CHANNEL_OPEN_EVENT_FN
 - cchannel/CHANNEL_OPEN_EVENT_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Cchannel.h
api_name:
 - CHANNEL_OPEN_EVENT_FN
---

# CHANNEL_OPEN_EVENT_FN callback function


## -description

An application-defined callback function that Remote Desktop Services calls to notify the client DLL of 
     events for a specific virtual channel.

The <b>PCHANNEL_OPEN_EVENT_FN</b> type defines a pointer to this callback function. 
    <b>VirtualChannelOpenEvent</b> is a 
    placeholder for the application-defined or library-defined function name.

## -parameters

### -param openHandle [in]

Handle to the virtual channel. This is the handle returned in the <i>pOpenHandle</i> 
      parameter of the <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelopen">VirtualChannelOpen</a> 
      function.

### -param event [in]

Indicates the event that caused the notification. This parameter can be one of the following values.



#### CHANNEL_EVENT_DATA_RECEIVED

The virtual channel received data from the server end. <i>pData</i> is a pointer to a 
        chunk of the data. <i>dataLength</i> indicates the size of this chunk. 
        <i>totalLength</i> indicates the total size of the data written by the server.



#### CHANNEL_EVENT_WRITE_CANCELLED

A write operation started by a 
         <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelwrite">VirtualChannelWrite</a> call has been 
         canceled. <i>pData</i> is the value specified in the <i>pUserData</i> 
         parameter of <b>VirtualChannelWrite</b>.

A write operation is canceled when the client session is disconnected. This notification enables you to 
         free any memory associated with the write operation.



#### CHANNEL_EVENT_WRITE_COMPLETE

A write operation started by a 
        <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelwrite">VirtualChannelWrite</a> call has 
        been completed. <i>pData</i> is the value specified in the 
        <i>pUserData</i> parameter of 
        <b>VirtualChannelWrite</b>.

### -param pData [in]

Pointer to additional data for the event. The type of data depends on the event, as described previously in 
       the event descriptions.

If <i>event</i> is <b>CHANNEL_EVENT_DATA_RECEIVED</b>, the data written 
       by the server is broken into chunks of not more than <b>CHANNEL_CHUNK_LENGTH</b> bytes. The 
       <i>dataFlags</i> parameter indicates whether the current chunk is at the beginning, middle, 
       or end of the block of data written by the server.

Note that the size of this parameter can be greater 
       than the value specified by the <i>dataLength</i> parameter. The application should read 
       only the number of bytes specified by <i>dataLength</i>.

### -param dataLength [in]

Specifies the size, in bytes, of the data in the <i>pData</i> buffer.

### -param totalLength [in]

Specifies the total size, in bytes, of the data written by a single write operation to the server end of 
      the virtual channel.

### -param dataFlags [in]

Provides information about the chunk of data being received in a 
       <b>CHANNEL_EVENT_DATA_RECEIVED</b> event. The following bit flags will be set.

Note that you should not make direct comparisons using the '==' operator when comparing the values in the 
       following list; instead, use the comparison methods described.



#### CHANNEL_FLAG_FIRST

The chunk is the beginning of the data written by a single write operation.

Use bitwise comparisons when comparing this flag.



#### CHANNEL_FLAG_LAST

The chunk is the end of the data written by a single write operation.

Use bitwise comparisons when comparing this flag.



#### CHANNEL_FLAG_MIDDLE

This is the default. The chunk is in the middle of a block of data written by a single write operation.

Do not use bitwise comparisons to compare this flag value directly. Instead, use bitwise comparisons to 
         determine that the flag value is not <b>CHANNEL_FLAG_FIRST</b> or 
         <b>CHANNEL_FLAG_LAST</b>. This is done by using the following comparison: 
         <code>Result = !(flags &amp; CHANNEL_FLAG_FIRST) &amp;&amp; !(flags &amp; CHANNEL_FLAG_LAST)</code>.



#### CHANNEL_FLAG_ONLY

Combines the <b>CHANNEL_FLAG_FIRST</b> and <b>CHANNEL_FLAG_LAST</b> 
         values. The chunk contains all the data from a single write operation.

Use bitwise comparisons when comparing this flag.

## -returns

This function has no return values.

## -remarks

The client DLL uses the 
    <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelopen">VirtualChannelOpen</a> function to 
    register a <b>VirtualChannelOpenEvent</b> 
    function for a specific virtual channel.

You can use the same 
    <b>VirtualChannelOpenEvent</b> function for 
    multiple calls to <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelopen">VirtualChannelOpen</a>.

This function can be called with a different event type while it is executing. For example, it might be called 
    with <b>CHANNEL_EVENT_WRITE_COMPLETE</b> or 
    <b>CHANNEL_EVENT_WRITE_CANCELLED</b> while it is processing the 
    <b>CHANNEL_EVENT_DATA_RECEIVED</b> event. Note that this function will not be called with the 
    same event type that it is currently processing.

## -see-also

<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelopen">VirtualChannelOpen</a>