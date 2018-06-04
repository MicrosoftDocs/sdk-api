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

# WMT_STATUS enumeration


## -description



The <b>WMT_STATUS</b> enumeration type defines a range of file status information. Members of <b>WMT_STATUS</b> are passed to the common callback function, <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a>, so that the application can respond to the changing status of the objects being used.




## -enum-fields




### -field WMT_ERROR

An error occurred.


### -field WMT_OPENED

A file was opened.


### -field WMT_BUFFERING_START

The reader object is beginning to buffer content.


### -field WMT_BUFFERING_STOP

The reader object has finished buffering content.


### -field WMT_EOF

The end of the file has been reached. Both this member and the next one, <b>WMT_END_OF_FILE</b>, have the value 4.


### -field WMT_END_OF_FILE

The end of the file has been reached. Both this member and the previous one, <b>WMT_EOF</b>, have the value 4.


### -field WMT_END_OF_SEGMENT

The end of a segment has been encountered.


### -field WMT_END_OF_STREAMING

The end of a server-side playlist has been reached.


### -field WMT_LOCATING

The reader object is locating requested data.


### -field WMT_CONNECTING

A reporting object is connecting to server.


### -field WMT_NO_RIGHTS

There is no <a href="wmformat_glossary.htm">license</a> and the content is protected by version 1 digital rights management.


### -field WMT_MISSING_CODEC

The file loaded in the reader object contains compressed data for which no codec could be found. The <i>pValue</i> parameter in <b>OnStatus</b> contains a GUID. The first DWORD of this GUID contains the FOURCC or the format tag of the missing codec. The remaining bytes of the GUID can be ignored.

The <i>hr</i> parameter in <b>OnStatus</b> may equal S_OK, although a missing codec would normally be considered an error. Also, this event may be followed by WMT_STARTED with <i>hr</i> equal to S_OK, even if codecs are missing for every stream in the file. In that case, however, the application will not receive any decoded samples, and should stop the reader object.


### -field WMT_STARTED

A reporting object has begun operations.


### -field WMT_STOPPED

A reporting object has ceased operations.


### -field WMT_CLOSED

A file was closed.


### -field WMT_STRIDING

The reader object is playing content at above normal speed, or in reverse.


### -field WMT_TIMER

Timer event.


### -field WMT_INDEX_PROGRESS

Progress update from the indexer object.


### -field WMT_SAVEAS_START

The reader object has begun saving a file from a server.


### -field WMT_SAVEAS_STOP

The reader has stopped saving a file from a server.


### -field WMT_NEW_SOURCEFLAGS

The current file's header object contains certain attributes that are different from those of the previous file. This event is sent when playing a server-side playlist. Use the <a href="https://msdn.microsoft.com/649f9a73-c70a-4524-b577-366ade969f2f">IWMHeaderInfo</a> interface to query for any of the following attributes in a new file: <a href="https://msdn.microsoft.com/9e03025a-e2ab-47ba-8426-a573d85be6f6">Stridable</a>, <a href="https://msdn.microsoft.com/da2adf16-a9b5-4678-896e-2be8f5ca27e4">Broadcast</a>, <a href="https://msdn.microsoft.com/9653e368-4782-4506-9c44-54c9406b61b5">Seekable</a>, and <a href="https://msdn.microsoft.com/3b67288f-4f04-47a4-91ca-c456107d9d7b">HasImage</a>.


### -field WMT_NEW_METADATA

The current file's header object contains metadata attributes that are different from those of the previous file. This event is sent when playing a server-side playlist. Use the <a href="https://msdn.microsoft.com/649f9a73-c70a-4524-b577-366ade969f2f">IWMHeaderInfo</a> interface to query for any metadata attribute you are interested in.


### -field WMT_BACKUPRESTORE_BEGIN

A <a href="wmformat_glossary.htm">license</a> backup or restore has started.


### -field WMT_SOURCE_SWITCH

The next source in the playlist was opened.


### -field WMT_ACQUIRE_LICENSE

The <a href="wmformat_glossary.htm">license acquisition</a> process has completed. The <i>pValue</i> parameter in <b>OnStatus</b> contains a <a href="https://msdn.microsoft.com/7e8053d5-f3f5-4519-97f5-6dbd89982f3a">WM_GET_LICENSE_DATA</a> structure. The <b>hr</b> member of this structure indicates whether the license was successfully acquired.


### -field WMT_INDIVIDUALIZE

<a href="wmformat_glossary.htm">
              Individualization</a> status message.


### -field WMT_NEEDS_INDIVIDUALIZATION

The file loaded in the reader object cannot be played without a security update.


### -field WMT_NO_RIGHTS_EX

There is no <a href="wmformat_glossary.htm">license</a> and the content is protected by version 7 digital rights management.


### -field WMT_BACKUPRESTORE_END

A <a href="wmformat_glossary.htm">license</a> backup or restore has finished.


### -field WMT_BACKUPRESTORE_CONNECTING

The backup restorer object is connecting to a server.


### -field WMT_BACKUPRESTORE_DISCONNECTING

The backup restorer object is disconnecting from a server.


### -field WMT_ERROR_WITHURL

Error relating to the URL.


### -field WMT_RESTRICTED_LICENSE

The backup restorer object cannot back up one or more <a href="wmformat_glossary.htm">licenses</a> because the right has been disallowed by the content owner.


### -field WMT_CLIENT_CONNECT

Sent when a client (a playing application or server) connects to a writer network sink object. The <i>pValue</i> parameter of the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> callback is set to a <a href="https://msdn.microsoft.com/62a5bafd-cc49-4a60-be03-038920e5b073">WM_CLIENT_PROPERTIES</a> structure. New applications should wait for <b>WMT_CLIENT_CONNECT_EX</b> instead.


### -field WMT_CLIENT_DISCONNECT

Sent when a client (a playing application or server) disconnects from a writer network sink object. The <i>pValue</i> parameter of the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> callback is set to a <a href="https://msdn.microsoft.com/62a5bafd-cc49-4a60-be03-038920e5b073">WM_CLIENT_PROPERTIES</a> structure. The values in this structure are identical to those sent on connection. New applications should wait for <b>WMT_CLIENT_DISCONNECT_EX</b> instead.


### -field WMT_NATIVE_OUTPUT_PROPS_CHANGED

Change in output properties.


### -field WMT_RECONNECT_START

Start of automatic reconnection to a server.


### -field WMT_RECONNECT_END

End of automatic reconnection to a server.


### -field WMT_CLIENT_CONNECT_EX

Sent when a client (a playing application or server) connects to a writer network sink object. The <i>pValue</i> parameter of the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> callback is set to a <a href="https://msdn.microsoft.com/981a466d-576b-4774-bd7b-785b0ef80e72">WM_CLIENT_PROPERTIES_EX</a> structure.


### -field WMT_CLIENT_DISCONNECT_EX

Sent when a client (a playing application or server) disconnects from a writer network sink object. The <i>pValue</i> parameter of the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> callback is set to a <a href="https://msdn.microsoft.com/981a466d-576b-4774-bd7b-785b0ef80e72">WM_CLIENT_PROPERTIES_EX</a> structure. The client properties are identical to those sent on connection except for the <b>pwszDNSName</b> member, which may have changed.


### -field WMT_SET_FEC_SPAN

Change to the forward error correction span.


### -field WMT_PREROLL_READY

The reader is ready to begin buffering content.


### -field WMT_PREROLL_COMPLETE

The reader is finished buffering.


### -field WMT_CLIENT_PROPERTIES

Sent by a writer network sink when one or more properties of a connected client changes. The <i>pValue</i> parameter of the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> callback is set to a <a href="https://msdn.microsoft.com/981a466d-576b-4774-bd7b-785b0ef80e72">WM_CLIENT_PROPERTIES_EX</a> structure. This usually means that a DNS name is present for a client for which none was available at connection.


### -field WMT_LICENSEURL_SIGNATURE_STATE

Sent before a <b>WMT_NO_RIGHTS</b> or <b>WMT_NO_RIGHTS_EX</b> status message. The <i>pValue</i> parameter is set to one of the <a href="https://msdn.microsoft.com/48c62532-1cb5-4073-8fa9-cab5a8355bc3">WMT_DRMLA_TRUST</a> constants indicating whether the <a href="wmformat_glossary.htm">license acquisition</a> URL is completely trusted.


### -field WMT_INIT_PLAYLIST_BURN

Sent when the <a href="https://msdn.microsoft.com/a20a70af-49bc-408f-8c64-779525436f8d">IWMReaderPlaylistBurn::InitPlaylistBurn</a> method returns.


### -field WMT_TRANSCRYPTOR_INIT

Sent when the DRM transcryptor object is initialized with a file.


### -field WMT_TRANSCRYPTOR_SEEKED

Sent when the DRM transcryptor object seeks to a point in a file.


### -field WMT_TRANSCRYPTOR_READ

Sent when the DRM transcryptor object delivers Windows Media DRM 10 for Network Devices data from a DRM-protected file.


### -field WMT_TRANSCRYPTOR_CLOSED

Sent when the DRM transcryptor object is closed. After receiving this message, you can release the interface.


### -field WMT_PROXIMITY_RESULT

Sent when the proximity detection protocol has finished.


### -field WMT_PROXIMITY_COMPLETED

Sent when proximity detection thread has stopped running. The application must not release the <a href="https://msdn.microsoft.com/0897ad8f-8e06-4de9-840e-1588e0e20c54">IWMProximityDetection</a> interface until this message is received. Once launched, the thread runs for two minutes; there is no way to terminate the thread before two minutes have elapsed.



### -field WMT_CONTENT_ENABLER

Sent when a content enabler is required.


## -remarks



For more information on how this enumeration type is used, see the Remarks section for the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> method.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

