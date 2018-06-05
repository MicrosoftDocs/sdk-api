---
UID: NE:webservices.WS_MESSAGE_PROPERTY_ID
title: WS_MESSAGE_PROPERTY_ID
author: windows-sdk-content
description: Each message property is of type WS_MESSAGE_PROPERTY, is identified by an ID, and has an associated value.
old-location: wsw\ws_message_property_id.htm
old-project: wsw
ms.assetid: 7398225c-afbd-45c6-9a32-8b8892f0ff8a
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_MESSAGE_PROPERTY_ADDRESSING_VERSION, WS_MESSAGE_PROPERTY_BODY_READER, WS_MESSAGE_PROPERTY_BODY_WRITER, WS_MESSAGE_PROPERTY_ENCODED_CERT, WS_MESSAGE_PROPERTY_ENVELOPE_VERSION, WS_MESSAGE_PROPERTY_HEADER_BUFFER, WS_MESSAGE_PROPERTY_HEADER_POSITION, WS_MESSAGE_PROPERTY_HEAP, WS_MESSAGE_PROPERTY_HEAP_PROPERTIES, WS_MESSAGE_PROPERTY_HTTP_HEADER_AUTH_WINDOWS_TOKEN, WS_MESSAGE_PROPERTY_ID, WS_MESSAGE_PROPERTY_ID enumeration [Web Services for Windows], WS_MESSAGE_PROPERTY_IS_ADDRESSED, WS_MESSAGE_PROPERTY_IS_FAULT, WS_MESSAGE_PROPERTY_MAX_PROCESSED_HEADERS, WS_MESSAGE_PROPERTY_MESSAGE_SECURITY_WINDOWS_TOKEN, WS_MESSAGE_PROPERTY_PROTECTION_LEVEL, WS_MESSAGE_PROPERTY_SAML_ASSERTION, WS_MESSAGE_PROPERTY_SECURITY_CONTEXT, WS_MESSAGE_PROPERTY_STATE, WS_MESSAGE_PROPERTY_TRANSPORT_SECURITY_WINDOWS_TOKEN, WS_MESSAGE_PROPERTY_USERNAME, WS_MESSAGE_PROPERTY_XML_READER_PROPERTIES, WS_MESSAGE_PROPERTY_XML_WRITER_PROPERTIES, webservices/WS_MESSAGE_PROPERTY_ADDRESSING_VERSION, webservices/WS_MESSAGE_PROPERTY_BODY_READER, webservices/WS_MESSAGE_PROPERTY_BODY_WRITER, webservices/WS_MESSAGE_PROPERTY_ENCODED_CERT, webservices/WS_MESSAGE_PROPERTY_ENVELOPE_VERSION, webservices/WS_MESSAGE_PROPERTY_HEADER_BUFFER, webservices/WS_MESSAGE_PROPERTY_HEADER_POSITION, webservices/WS_MESSAGE_PROPERTY_HEAP, webservices/WS_MESSAGE_PROPERTY_HEAP_PROPERTIES, webservices/WS_MESSAGE_PROPERTY_HTTP_HEADER_AUTH_WINDOWS_TOKEN, webservices/WS_MESSAGE_PROPERTY_ID, webservices/WS_MESSAGE_PROPERTY_IS_ADDRESSED, webservices/WS_MESSAGE_PROPERTY_IS_FAULT, webservices/WS_MESSAGE_PROPERTY_MAX_PROCESSED_HEADERS, webservices/WS_MESSAGE_PROPERTY_MESSAGE_SECURITY_WINDOWS_TOKEN, webservices/WS_MESSAGE_PROPERTY_PROTECTION_LEVEL, webservices/WS_MESSAGE_PROPERTY_SAML_ASSERTION, webservices/WS_MESSAGE_PROPERTY_SECURITY_CONTEXT, webservices/WS_MESSAGE_PROPERTY_STATE, webservices/WS_MESSAGE_PROPERTY_TRANSPORT_SECURITY_WINDOWS_TOKEN, webservices/WS_MESSAGE_PROPERTY_USERNAME, webservices/WS_MESSAGE_PROPERTY_XML_READER_PROPERTIES, webservices/WS_MESSAGE_PROPERTY_XML_WRITER_PROPERTIES, wsw.ws_message_property_id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WS_MESSAGE_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_MESSAGE_PROPERTY_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_MESSAGE_PROPERTY_ID enumeration


## -description



                Each message property is of type <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a>, is identified by an ID, and has an associated
                value.
            


## -enum-fields




### -field WS_MESSAGE_PROPERTY_STATE


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is the current <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE</a> of the message.


                    This property is available in all message states.
                


### -field WS_MESSAGE_PROPERTY_HEAP


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is the <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a> of the message.  The heap is
                    owned by the message.  A user of a message is free to make additional
                    allocations within this heap.  Allocations within the heap are free'd
                    when a message is reset/freed.
                


                    The user of the returned heap should not call <a href="https://msdn.microsoft.com/c927ccb9-66c8-4acf-bbb5-12313ea80ee0">WsResetHeap</a>
                    on the heap.  This will result in undefined behavior.
                


                    The message object will not use the heap object unless one of
                    the message APIs is invoked.
                


                    This property is available in all message states except <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>. 
                    Using the heap of an empty message will result in undefined behavior.
                


### -field WS_MESSAGE_PROPERTY_ENVELOPE_VERSION


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a>.
                


                    The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure  is the <a href="https://msdn.microsoft.com/2a6f6148-d37d-4ac2-8fd0-409eae71a3d8">WS_ENVELOPE_VERSION</a> of the message.
                


                    When creating a message using <a href="https://msdn.microsoft.com/1c48647e-9e77-4b7a-add3-e035c7f9f27e">WsCreateMessage</a>, the
                    envelope version is specified as an explicit parameter (instead
                    of as a property).
                


                    This property may be specified when message properties are specified using
                    the <a href="https://msdn.microsoft.com/74ad74fd-457a-4408-8032-15d365f98b14">WS_MESSAGE_PROPERTIES</a> structure.
                


                    This property is available in all message states except <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
                


### -field WS_MESSAGE_PROPERTY_ADDRESSING_VERSION


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a>.
                


                    The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure  is the <a href="https://msdn.microsoft.com/87f60067-109c-456c-b060-33ab840872e0">WS_ADDRESSING_VERSION</a> of the message.
                


                    When creating a message using <a href="https://msdn.microsoft.com/1c48647e-9e77-4b7a-add3-e035c7f9f27e">WsCreateMessage</a>, the
                    addressing version is specified as an explicit parameter (instead
                    of as a property).
                


                    This property may be specified when message properties are specified using 
                    the <a href="https://msdn.microsoft.com/74ad74fd-457a-4408-8032-15d365f98b14">WS_MESSAGE_PROPERTIES</a> structure.
                


                    This property is available in all message states except <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
                


### -field WS_MESSAGE_PROPERTY_HEADER_BUFFER


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a>.
                


                    The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure  is a <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> that holds the headers
                    of the message (as well as the envelope and body elements).
                


                    This buffer is valid until the message is reset/freed.
                


                    This property is available in all message states except <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
                


### -field WS_MESSAGE_PROPERTY_HEADER_POSITION


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a>.

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure  is the <a href="https://msdn.microsoft.com/40ca058c-04e1-4358-b330-360a094a8791">WS_XML_NODE_POSITION</a>
                    of the header element within the header buffer (the element that contains all
                    the message headers as children).  The header buffer itself can be
                    obtained using <a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_HEADER_BUFFER</a>.
                


                    An application can use the <a href="https://msdn.microsoft.com/40ca058c-04e1-4358-b330-360a094a8791">WS_XML_NODE_POSITION</a> returned as a starting 
                    point when reading or writing headers manually (when not using <a href="https://msdn.microsoft.com/34671c47-d21e-47c4-9fb0-10b036fb4f70">WsSetHeader</a>, 
                    <a href="https://msdn.microsoft.com/ff6e639f-715d-4a4f-b0ef-35202aa54dc5">WsGetHeader</a>, <a href="https://msdn.microsoft.com/bdfb441b-afc4-4be8-b437-f299a31ce84b">WsGetCustomHeader</a> or <a href="https://msdn.microsoft.com/4b95085a-e522-4ab2-b7c9-d332599c5598">WsAddCustomHeader</a>).  
                    For example, the position can be passed to <a href="https://msdn.microsoft.com/1d23bda1-d1da-44d4-9a9d-258bba200b29">WsSetWriterPosition</a> or 
                    <a href="https://msdn.microsoft.com/cc879cc0-c8ca-457e-9ff1-ae220e31cb04">WsSetReaderPosition</a> to position an <a href="https://msdn.microsoft.com/1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2">XML Reader</a> or <a href="https://msdn.microsoft.com/69d50793-1d5b-4fc7-bf69-128f8e23a98d">XML Writer</a>
                    within the <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> containining the headers.  Additionally, 
                    <a href="https://msdn.microsoft.com/63d18407-f82b-4884-a162-2c8163e883e1">WsMoveReader</a> or <a href="https://msdn.microsoft.com/f8eace53-9fa5-466a-8894-3c8b8fe049e3">WsMoveWriter</a> can be used to move relative 
                    to the position that was set.
                


                    When the headers of a message are read (via <a href="https://msdn.microsoft.com/e4f92e99-f272-47b5-8eaa-56713b22df7e">WsReadMessageStart</a> or
                    <a href="https://msdn.microsoft.com/f2b20e6b-fac0-47b0-8ce9-ad06dc93f0e6">WsReadEnvelopeStart</a>, a header element is automatically added to the 
                    header buffer if one is not present in the message being read.  When a message is initialized
                    (via <a href="https://msdn.microsoft.com/26eafc5f-6636-4f96-a037-7935cdac5900">WsInitializeMessage</a>), a header element is added automatically
                    to the message.
                


                    This property is available in all message states except <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
                


                    The header position is valid until the message is reset or freed.
                


### -field WS_MESSAGE_PROPERTY_BODY_READER


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a>.
                


                    The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure  is a <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> that can be used to read
                    the body of the message.
                


                    The reader is owned by the message object, and is valid only 
                    until either <a href="https://msdn.microsoft.com/50e08300-9445-4741-9298-bd80fc777041">WsFreeMessage</a> or <a href="https://msdn.microsoft.com/90a62cc8-a7e0-4451-8490-f6384bf3e7b6">WsResetMessage</a> are called.
                


                    This property is only available when the message is 
                    in <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_READING</a> state.
                


### -field WS_MESSAGE_PROPERTY_BODY_WRITER


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a>.
                


                    The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure  is a <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> that can be used to write
                    the body of the message.
                


                    This property is only available when the message is in 
                    <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_WRITING</a> state.
                


                    The writer is owned by the message object, and is valid only
                    until either <a href="https://msdn.microsoft.com/50e08300-9445-4741-9298-bd80fc777041">WsFreeMessage</a> or <a href="https://msdn.microsoft.com/90a62cc8-a7e0-4451-8490-f6384bf3e7b6">WsResetMessage</a> are called.
                


### -field WS_MESSAGE_PROPERTY_IS_ADDRESSED


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a>.
                


                    The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure  is a <b>BOOL</b> indicating whether the message has
                    been addressed.
                


                    When a message is created or reset, this property is
                    set to <b>FALSE</b>.
                


                    When a message is read (<a href="https://msdn.microsoft.com/e4f92e99-f272-47b5-8eaa-56713b22df7e">WsReadMessageStart</a> or
                    <a href="https://msdn.microsoft.com/f2b20e6b-fac0-47b0-8ce9-ad06dc93f0e6">WsReadEnvelopeStart</a>, then this property is
                    set to <b>TRUE</b>.
                


                    This property is available in all message states except <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
                


                    See <a href="https://msdn.microsoft.com/30b2dbd1-7232-4ff1-b30a-920df8bfe423">WsAddressMessage</a> for more information.
                


### -field WS_MESSAGE_PROPERTY_HEAP_PROPERTIES


                    This property is used with <a href="https://msdn.microsoft.com/1c48647e-9e77-4b7a-add3-e035c7f9f27e">WsCreateMessage</a> to specify the properties
                    of the <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a> associated with the message.
                


                    The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is of type <a href="https://msdn.microsoft.com/d367bb85-514d-4acc-b67f-f7381a9a6404">WS_HEAP_PROPERTIES</a>.
                


                    The heap is used to buffer the headers of the message.
                


                    The following heap properties may be specified:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/c047a3b9-27a1-464c-b9f9-0b0c6cf8eb97">WS_HEAP_PROPERTY_MAX_SIZE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c047a3b9-27a1-464c-b9f9-0b0c6cf8eb97">WS_HEAP_PROPERTY_TRIM_SIZE</a>
</li>
</ul>

### -field WS_MESSAGE_PROPERTY_XML_READER_PROPERTIES


                    This property is used with <a href="https://msdn.microsoft.com/1c48647e-9e77-4b7a-add3-e035c7f9f27e">WsCreateMessage</a> to specify properties 
                    that apply to <a href="https://msdn.microsoft.com/1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2">XML Readers</a> that are used with the message.
                


                    These XML Reader properties are used by the message object when reading headers.
                    In addition, channels use these properties for the readers that they create to read
                    messages.
                


                    The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is of type <a href="https://msdn.microsoft.com/5373c8d3-9201-417e-99d9-cc0d15a35ea6">WS_XML_READER_PROPERTIES</a>.
                


                    The following properties may be specified:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/b8d36716-e25a-4215-8bc7-30091b68c0f6">WS_XML_READER_PROPERTY_MAX_DEPTH</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b8d36716-e25a-4215-8bc7-30091b68c0f6">WS_XML_READER_PROPERTY_MAX_ATTRIBUTES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b8d36716-e25a-4215-8bc7-30091b68c0f6">WS_XML_READER_PROPERTY_READ_DECLARATION</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b8d36716-e25a-4215-8bc7-30091b68c0f6">WS_XML_READER_PROPERTY_UTF8_TRIM_SIZE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b8d36716-e25a-4215-8bc7-30091b68c0f6">WS_XML_READER_PROPERTY_STREAM_BUFFER_SIZE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b8d36716-e25a-4215-8bc7-30091b68c0f6">WS_XML_READER_PROPERTY_STREAM_MAX_ROOT_MIME_PART_SIZE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b8d36716-e25a-4215-8bc7-30091b68c0f6">WS_XML_READER_PROPERTY_STREAM_MAX_MIME_HEADERS_SIZE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b8d36716-e25a-4215-8bc7-30091b68c0f6">WS_XML_READER_PROPERTY_MAX_MIME_PARTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b8d36716-e25a-4215-8bc7-30091b68c0f6">WS_XML_READER_PROPERTY_ALLOW_INVALID_CHARACTER_REFERENCES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b8d36716-e25a-4215-8bc7-30091b68c0f6">WS_XML_READER_PROPERTY_MAX_NAMESPACES</a>
</li>
</ul>

### -field WS_MESSAGE_PROPERTY_XML_WRITER_PROPERTIES


                    This property is used with <a href="https://msdn.microsoft.com/1c48647e-9e77-4b7a-add3-e035c7f9f27e">WsCreateMessage</a> to specify the properties
                    of the <a href="https://msdn.microsoft.com/69d50793-1d5b-4fc7-bf69-128f8e23a98d">XML Writers</a> that are used with the message.
                


                    These XML Writer properties are used by the message object when writing headers.
                    In addition, channels use these properties for the wrtiers that they create to write
                    messages.
                


                    The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is of type <a href="https://msdn.microsoft.com/8c874422-3d59-43cd-b65e-8f4f543e57e5">WS_XML_WRITER_PROPERTIES</a>.
                


                    The following properties may be specified:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_MAX_DEPTH</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_MAX_ATTRIBUTES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_WRITE_DECLARATION</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_BUFFER_TRIM_SIZE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_MAX_MIME_PARTS_BUFFER_SIZE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_ALLOW_INVALID_CHARACTER_REFERENCES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_MAX_NAMESPACES</a>
</li>
</ul>

### -field WS_MESSAGE_PROPERTY_IS_FAULT


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a> or <a href="https://msdn.microsoft.com/f1e6616f-63ac-4afb-90dd-17a776d59eeb">WsSetMessageProperty</a>
                    to indicate whether a message contains a fault.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is a <b>BOOL</b>.


                    When a message is read (<a href="https://msdn.microsoft.com/e4f92e99-f272-47b5-8eaa-56713b22df7e">WsReadMessageStart</a> or <a href="https://msdn.microsoft.com/f2b20e6b-fac0-47b0-8ce9-ad06dc93f0e6">WsReadEnvelopeStart</a>),
                    this property is set according to whether the first element of the body is a fault
                    element.  An application can test this property as a way of deciding whether
                    to read the body as a fault.  To read the body as a fault, use <a href="https://msdn.microsoft.com/43ceeb1e-aeb2-4482-90f0-d7f6013b239f">WsReadBody</a> 
                    with <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_FAULT_TYPE</a> to obtain a <a href="https://msdn.microsoft.com/7fe0b142-04a1-4a92-99ca-523412f7c94e">WS_FAULT</a>.
                


                    When a message is written (<a href="https://msdn.microsoft.com/43cc43a5-7853-4170-911d-e514ac722da5">WsWriteMessageStart</a> or <a href="https://msdn.microsoft.com/213fe780-82f2-4140-92f2-2665317a5cb6">WsWriteEnvelopeStart</a>)
                    this property can be used to indicate whether or not the application will write a fault
                    in the body.  Some channels will use this information in order to determine how to 
                    send the message.  For example, HTTP will send a 500 status code for faults instead of 200.
                


                    When a message is initialized using <a href="https://msdn.microsoft.com/26eafc5f-6636-4f96-a037-7935cdac5900">WsInitializeMessage</a> with
                    <a href="https://msdn.microsoft.com/f4a674c1-4017-49c8-aa9a-68f1d2b84378">WS_FAULT_MESSAGE</a>, the property is set to <b>TRUE</b>.  
                    For other <b>WS_MESSAGE_INITIALIZATION</b> values, the property is set to <b>FALSE</b>.
                


                    This property is available in all message states except <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
                


### -field WS_MESSAGE_PROPERTY_MAX_PROCESSED_HEADERS


                    This property is used with <a href="https://msdn.microsoft.com/1c48647e-9e77-4b7a-add3-e035c7f9f27e">WsCreateMessage</a> to specify the maximum number of headers
                    that will be allowed when processing the message headers.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is a <b>ULONG</b>.


                    The purpose of this limit is to put an upper bound on the number of iterations 
                    spent scanning for a header.
                


                    Since an application can directly modify the contents of the header buffer,
                    this limit is not enforced in all cases.  It is only enforced when one of 
                    the header access APIs are used (<a href="https://msdn.microsoft.com/34671c47-d21e-47c4-9fb0-10b036fb4f70">WsSetHeader</a>, <a href="https://msdn.microsoft.com/ff6e639f-715d-4a4f-b0ef-35202aa54dc5">WsGetHeader</a>, 
                    <a href="https://msdn.microsoft.com/bdfb441b-afc4-4be8-b437-f299a31ce84b">WsGetCustomHeader</a>, or <a href="https://msdn.microsoft.com/abdff5ca-fb0d-4867-b729-5cfe18520f80">WsGetMappedHeader</a>).
                


                    The default value is 64.
                


### -field WS_MESSAGE_PROPERTY_USERNAME


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a> to retrieve the sender's
                    username from a received message, if username/password based security
                    is on, or if a custom channel has set the value.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is a <a href="https://msdn.microsoft.com/eb6c7397-6b15-4e79-89ec-585861113edf">WS_STRING</a> structure.


                    The returned value is good until the message is freed or reset.
                


                    A custom channel can use <a href="https://msdn.microsoft.com/f1e6616f-63ac-4afb-90dd-17a776d59eeb">WsSetMessageProperty</a> to set
                    the sender's username from the message if it supports username/password
                    based security.  The function will make a copy of the value specified.
                


                    This property is available in all message states except 
                    <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
                


### -field WS_MESSAGE_PROPERTY_ENCODED_CERT


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a> to retrieve the sender's
                    certificate from a received message as encoded bytes, if
                    a certificate-based security mode (such as SSL) is on, 
                    or if a custom channel has set the value.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is a <a href="https://msdn.microsoft.com/0106e372-80bf-4a62-b941-1a4501c92a9c">WS_BYTES</a> structure.


                    The returned value is good until the message is freed or reset.
                


                    A custom channel can use <a href="https://msdn.microsoft.com/f1e6616f-63ac-4afb-90dd-17a776d59eeb">WsSetMessageProperty</a> to set
                    the sender's certificate from a received message if it supports
                    a certificate-based security mode.  The function will make a copy of the value specified.
                


                    This property is available in all message states except
                    <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
                


### -field WS_MESSAGE_PROPERTY_TRANSPORT_SECURITY_WINDOWS_TOKEN


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a> to retrieve the Windows
                    token representing the sender from a received message.  This property is 
                    available in the following cases:
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is a <b>HANDLE</b>.

<ul>
<li>
<a href="https://msdn.microsoft.com/c617f6cf-cedb-4d52-954c-fd4577260ca3">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a> is being used.
                    </li>
<li>
<a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> is being used 
                    and the translation from client certificate to Windows token
                    has been enabled at the http.sys config level.
                    </li>
<li>A custom channel implementation has set the value.
                </li>
</ul>

                    The returned value is good until the message is freed or reset.
                


                    A custom channel can use <a href="https://msdn.microsoft.com/f1e6616f-63ac-4afb-90dd-17a776d59eeb">WsSetMessageProperty</a> to set
                    the sender's certificate from a received message if it supports
                    a certificate-based security mode.  The function will duplicate the handle specified.
                


                    This property is available in all message states except
                    <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
                


### -field WS_MESSAGE_PROPERTY_HTTP_HEADER_AUTH_WINDOWS_TOKEN


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a> to retrieve the Windows
                    token representing the sender from a received message, if the
                    <a href="https://msdn.microsoft.com/c6ca6760-a927-470f-9785-7500d1711902">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a> is used,
                    or if a custom channel has set the value.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is a <b>HANDLE</b>.


                    The returned value is good until the message is freed or reset.
                


                    A custom channel can use <a href="https://msdn.microsoft.com/f1e6616f-63ac-4afb-90dd-17a776d59eeb">WsSetMessageProperty</a>to set
                    the windows token representing the sender from a received message.
                    The function will duplicate the handle specified.
                


                    This property is available in all message states except
                    <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
                


### -field WS_MESSAGE_PROPERTY_MESSAGE_SECURITY_WINDOWS_TOKEN


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a> to retrieve the Windows
                    token representing the sender from a received message, if a message security
                    binding such as <a href="https://msdn.microsoft.com/03127248-f5cc-44da-9c3d-abf016dd6bb2">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a> is used,
                    or if a custom channel has set the value.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is a <b>HANDLE</b>.


                    The returned value is good until the message is freed or reset.
                


                    A custom channel can use <a href="https://msdn.microsoft.com/f1e6616f-63ac-4afb-90dd-17a776d59eeb">WsSetMessageProperty</a> to set
                    the token representing the sender from a received message.
                    The function will duplicate the handle specified.
                


                    This property is available in all message states except
                    <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
                


### -field WS_MESSAGE_PROPERTY_SAML_ASSERTION


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a> to retrieve the SAML assertion
                    representing the sender from a received message, if the
                    <a href="https://msdn.microsoft.com/713afe9a-49b8-419a-b78b-d3b5a4a8d073">WS_SAML_MESSAGE_SECURITY_BINDING</a> is used on the server side,
                    or if a custom channel has set the value.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is a <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a>.


                    The returned value is good until the message is freed or reset.
                


                    A custom channel can use <a href="https://msdn.microsoft.com/f1e6616f-63ac-4afb-90dd-17a776d59eeb">WsSetMessageProperty</a> to set
                    the SAML assertion representing the sender from a received message.
                    The function will duplicate the buffer specified.
                


                    This property is available in all message states except
                    <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
                


### -field WS_MESSAGE_PROPERTY_SECURITY_CONTEXT


                    This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a> to retrieve the secure conversation handle if the
                    <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a> is used on the server side.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is a <a href="https://msdn.microsoft.com/8d23357b-bff8-45fe-80ef-df3f3b0edde1">WS_SECURITY_CONTEXT</a>.


                    The returned value is good until the message is freed or reset.
                


### -field WS_MESSAGE_PROPERTY_PROTECTION_LEVEL


                This property is used with <a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a> to retrieve the message's security protection level.

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structure is a <a href="https://msdn.microsoft.com/2b673728-1050-4005-bbb6-64b81ec19174">WS_PROTECTION_LEVEL</a> value.


                 If the channel does not use security, or if security verification failed, the protection level is set to 
                <a href="https://msdn.microsoft.com/2b673728-1050-4005-bbb6-64b81ec19174">WS_PROTECTION_LEVEL_NONE</a>. Otherwise it is set to the level requested by the application.            
            


                This property may be used to dermine the status of the security verification when <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_ALLOW_UNSECURED_FAULTS</a> 
                is set to <b>FALSE</b>.
            


                A custom channel can use <a href="https://msdn.microsoft.com/f1e6616f-63ac-4afb-90dd-17a776d59eeb">WsSetMessageProperty</a> to set
                the protection level of a received message.
            


                This property is available in all message states except
                <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
            

