---
UID: NE:webservices.WS_XML_WRITER_PROPERTY_ID
title: WS_XML_WRITER_PROPERTY_ID
author: windows-driver-content
description: Each xml writer property is identified by an ID and has an associated value.
old-location: wsw\ws_xml_writer_property_id.htm
old-project: wsw
ms.assetid: c919eb01-bd15-4583-afcf-e46ac2fc9c8c
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_XML_WRITER_PROPERTY_ALLOW_FRAGMENT, WS_XML_WRITER_PROPERTY_ALLOW_INVALID_CHARACTER_REFERENCES, WS_XML_WRITER_PROPERTY_BUFFERS, WS_XML_WRITER_PROPERTY_BUFFER_MAX_SIZE, WS_XML_WRITER_PROPERTY_BUFFER_TRIM_SIZE, WS_XML_WRITER_PROPERTY_BYTES, WS_XML_WRITER_PROPERTY_BYTES_TO_CLOSE, WS_XML_WRITER_PROPERTY_BYTES_WRITTEN, WS_XML_WRITER_PROPERTY_CHARSET, WS_XML_WRITER_PROPERTY_COMPRESS_EMPTY_ELEMENTS, WS_XML_WRITER_PROPERTY_EMIT_UNCOMPRESSED_EMPTY_ELEMENTS, WS_XML_WRITER_PROPERTY_ID, WS_XML_WRITER_PROPERTY_ID enumeration [Web Services for Windows], WS_XML_WRITER_PROPERTY_INDENT, WS_XML_WRITER_PROPERTY_INITIAL_BUFFER, WS_XML_WRITER_PROPERTY_IN_ATTRIBUTE, WS_XML_WRITER_PROPERTY_MAX_ATTRIBUTES, WS_XML_WRITER_PROPERTY_MAX_DEPTH, WS_XML_WRITER_PROPERTY_MAX_MIME_PARTS_BUFFER_SIZE, WS_XML_WRITER_PROPERTY_MAX_NAMESPACES, WS_XML_WRITER_PROPERTY_WRITE_DECLARATION, webservices/WS_XML_WRITER_PROPERTY_ALLOW_FRAGMENT, webservices/WS_XML_WRITER_PROPERTY_ALLOW_INVALID_CHARACTER_REFERENCES, webservices/WS_XML_WRITER_PROPERTY_BUFFERS, webservices/WS_XML_WRITER_PROPERTY_BUFFER_MAX_SIZE, webservices/WS_XML_WRITER_PROPERTY_BUFFER_TRIM_SIZE, webservices/WS_XML_WRITER_PROPERTY_BYTES, webservices/WS_XML_WRITER_PROPERTY_BYTES_TO_CLOSE, webservices/WS_XML_WRITER_PROPERTY_BYTES_WRITTEN, webservices/WS_XML_WRITER_PROPERTY_CHARSET, webservices/WS_XML_WRITER_PROPERTY_COMPRESS_EMPTY_ELEMENTS, webservices/WS_XML_WRITER_PROPERTY_EMIT_UNCOMPRESSED_EMPTY_ELEMENTS, webservices/WS_XML_WRITER_PROPERTY_ID, webservices/WS_XML_WRITER_PROPERTY_INDENT, webservices/WS_XML_WRITER_PROPERTY_INITIAL_BUFFER, webservices/WS_XML_WRITER_PROPERTY_IN_ATTRIBUTE, webservices/WS_XML_WRITER_PROPERTY_MAX_ATTRIBUTES, webservices/WS_XML_WRITER_PROPERTY_MAX_DEPTH, webservices/WS_XML_WRITER_PROPERTY_MAX_MIME_PARTS_BUFFER_SIZE, webservices/WS_XML_WRITER_PROPERTY_MAX_NAMESPACES, webservices/WS_XML_WRITER_PROPERTY_WRITE_DECLARATION, wsw.ws_xml_writer_property_id
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WS_XML_WRITER_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_XML_WRITER_PROPERTY_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_XML_WRITER_PROPERTY_ID enumeration


## -description



        Each xml writer property is identified by an ID and has an associated value.
      This enumeration is used within the <a href="https://msdn.microsoft.com/2979d038-f0a8-407d-bf8e-dca4027f6410">WS_XML_WRITER_PROPERTY</a> structure, which is used as a parameter to <a href="https://msdn.microsoft.com/5b4bb009-764e-4892-903a-5939f5570016">WsCreateWriter</a>, <a href="https://msdn.microsoft.com/f0b47817-0ad1-408c-a6da-9a7b0fb2e34b">WsSetOutput</a>, <a href="https://msdn.microsoft.com/b969700d-7145-45eb-ad4b-c6e643975709">WsSetOutputToBuffer</a>, and <a href="https://msdn.microsoft.com/dea4bfa5-7cd0-440f-89fe-e46af116462e">WsWriteXmlBufferToBytes</a>. It is also used directly as a parameter to <a href="https://msdn.microsoft.com/1167662f-0383-44bb-a7e1-1ec12539903e">WsGetWriterProperty</a>.


## -enum-fields




### -field WS_XML_WRITER_PROPERTY_MAX_DEPTH


          A <b>ULONG</b> that specifies the maximum depth of the document that the writer will permit.
        


          Depth is measured at any point by the number of nested start elements.
        


          A depth of 0 prevents any start elements from being written.
        


          This property defaults to 32.
        


### -field WS_XML_WRITER_PROPERTY_ALLOW_FRAGMENT


          A <a href="https://msdn.microsoft.com/18236818-492f-4906-9e7d-6ca03ef28d36">WS_XML_WRITER_MTOM_ENCODING</a> structure that specifies whether the writer will permit multiple elements and non-white space at the top level of the document.  This property
          may not be set to <b>TRUE</b> with <b>WS_XML_WRITER_MTOM_ENCODING</b>.
        


          This property defaults to <b>FALSE</b>.
        


### -field WS_XML_WRITER_PROPERTY_MAX_ATTRIBUTES

A <b>ULONG</b> that specifies
          the maximum number of attributes the writer will permit on an element.
        


          This property defaults to 128.
        


### -field WS_XML_WRITER_PROPERTY_WRITE_DECLARATION


          A <b>BOOL</b> that specifies if the writer should emit an appropriate xml declaration at the start of the document.
        


          This property defaults to <b>FALSE</b>.
        


### -field WS_XML_WRITER_PROPERTY_INDENT

A <b>ULONG</b> that specifies the how many spaces of indenting should be used to format the xml.  If indent is zero, no formatting occurs.
        


          This property defaults to 0.
        


### -field WS_XML_WRITER_PROPERTY_BUFFER_TRIM_SIZE


          A <b>ULONG</b> that specifies one of the following.

If the writer is using <a href="https://msdn.microsoft.com/46c0595c-9aa5-47cf-931a-8dc35e265fa0">WS_XML_WRITER_BUFFER_OUTPUT</a>, then this property is the maximum number of bytes
          the writer will retain across calls to <a href="https://msdn.microsoft.com/f0b47817-0ad1-408c-a6da-9a7b0fb2e34b">WsSetOutput</a> for purposes of buffering output.
        


          If the writer is using <a href="https://msdn.microsoft.com/8ee4ea59-5cdc-43bf-80c0-8f8632fee274">WS_XML_WRITER_STREAM_OUTPUT</a>, then this property is the maximum number of bytes
          the writer will retain across calls to <a href="https://msdn.microsoft.com/f0b47817-0ad1-408c-a6da-9a7b0fb2e34b">WsSetOutput</a>  and <a href="https://msdn.microsoft.com/ba631942-d5a0-4d93-9899-c3f0ebd4aae5">WsFlushWriter</a> for
          purposes of buffering output.
        


          This property has no effect when specified with <a href="https://msdn.microsoft.com/b969700d-7145-45eb-ad4b-c6e643975709">WsSetOutputToBuffer</a>.
        


          This property defaults to 4096.
        


### -field WS_XML_WRITER_PROPERTY_CHARSET

A <a href="https://msdn.microsoft.com/47dadf5d-1bc7-4f93-936c-21c936bc3fc3">WS_CHARSET</a> value that
          returns the character set the writer is using to encode the document.  This value is only available for
          text documents.
        


### -field WS_XML_WRITER_PROPERTY_BUFFERS

A <a href="https://msdn.microsoft.com/17ea7ba4-42d4-41a0-8982-a44518199ea8">WS_BUFFERS</a> structure
          that returns a set of buffers containing the generated xml bytes.
        


          If the writer is using <a href="https://msdn.microsoft.com/46c0595c-9aa5-47cf-931a-8dc35e265fa0">WS_XML_WRITER_BUFFER_OUTPUT</a>, then the all the generated bytes are returned, and
          the buffers are valid until <a href="https://msdn.microsoft.com/f0b47817-0ad1-408c-a6da-9a7b0fb2e34b">WsSetOutput</a>  or <a href="https://msdn.microsoft.com/eb1eb835-838a-41e4-9e7d-c5c805237f65">WsFreeWriter</a> is called.
        


          If the writer is using <a href="https://msdn.microsoft.com/18236818-492f-4906-9e7d-6ca03ef28d36">WS_XML_WRITER_MTOM_ENCODING</a>, then there must be no open elements.
          The supporting MIME parts will be generated and included in the returned buffers.  Once this
          occurs, any API that attempts to write further to the xml document will return <b>WS_E_INVALID_OPERATION</b>.
        (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)


          This property is not available when using <a href="https://msdn.microsoft.com/8ee4ea59-5cdc-43bf-80c0-8f8632fee274">WS_XML_WRITER_STREAM_OUTPUT</a>.
        


          This property is not available on a writer that is set to a <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a>.
        


          This may be less convenient but more efficient than using <a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_BYTES</a> because the
          writer does not have to concatenate the buffers that comprise the document into a single buffer.
        


### -field WS_XML_WRITER_PROPERTY_BUFFER_MAX_SIZE

A <b>ULONG</b> that
          specifies the maximum number of bytes the writer will buffer.
        


          If the writer is using <a href="https://msdn.microsoft.com/46c0595c-9aa5-47cf-931a-8dc35e265fa0">WS_XML_WRITER_BUFFER_OUTPUT</a>, then this is the maximum number of
          bytes that will buffered for the entire document.  Calls to <a href="https://msdn.microsoft.com/ba631942-d5a0-4d93-9899-c3f0ebd4aae5">WsFlushWriter</a> have no effect.
        


          If the writer is using <a href="https://msdn.microsoft.com/8ee4ea59-5cdc-43bf-80c0-8f8632fee274">WS_XML_WRITER_STREAM_OUTPUT</a>, then this is the maxmimum amount of
          data that will be buffered between <a href="https://msdn.microsoft.com/ba631942-d5a0-4d93-9899-c3f0ebd4aae5">WsFlushWriter</a> calls.
        


          This property has no effect when specified with <a href="https://msdn.microsoft.com/b969700d-7145-45eb-ad4b-c6e643975709">WsSetOutputToBuffer</a>.
        


### -field WS_XML_WRITER_PROPERTY_BYTES

A <a href="https://msdn.microsoft.com/17ea7ba4-42d4-41a0-8982-a44518199ea8">WS_BUFFERS</a> structure
          that returns a single buffer containing the generated xml bytes.
        


          If the writer is using <a href="https://msdn.microsoft.com/46c0595c-9aa5-47cf-931a-8dc35e265fa0">WS_XML_WRITER_BUFFER_OUTPUT</a>, then all the generated bytes are returned, and
          the buffer is valid until <a href="https://msdn.microsoft.com/f0b47817-0ad1-408c-a6da-9a7b0fb2e34b">WsSetOutput</a>  or <a href="https://msdn.microsoft.com/eb1eb835-838a-41e4-9e7d-c5c805237f65">WsFreeWriter</a> is called.
        


          If the writer is using <a href="https://msdn.microsoft.com/18236818-492f-4906-9e7d-6ca03ef28d36">WS_XML_WRITER_MTOM_ENCODING</a>, then there must be no open elements.
          The supporting MIME parts will be generated and included in the returned buffers.  Once this
          occurs, any API that attempts to write further to the xml document will return <b>WS_E_INVALID_OPERATION</b>.
        


          This property is not available when using <a href="https://msdn.microsoft.com/8ee4ea59-5cdc-43bf-80c0-8f8632fee274">WS_XML_WRITER_STREAM_OUTPUT</a>.
        


          This property is not available on a writer that is set to a <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a>.
        


          This may be more convenient but less efficient than using <a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_BUFFERS</a> because the
          writer may need to concatenate the buffers that comprise the document into a single buffer.
        


### -field WS_XML_WRITER_PROPERTY_IN_ATTRIBUTE

A <b>BOOL</b> that
          indicates that <a href="https://msdn.microsoft.com/9fd1eed9-6d8b-4b2e-a7ad-54a7f584734f">WsWriteStartAttribute</a> has been called and the writer is
          positioned on attribute content.
        


### -field WS_XML_WRITER_PROPERTY_MAX_MIME_PARTS_BUFFER_SIZE


          A <b>ULONG</b> used with <a href="https://msdn.microsoft.com/18236818-492f-4906-9e7d-6ca03ef28d36">WS_XML_WRITER_MTOM_ENCODING</a>. This specifies the maximum amount of data that
          will be buffered for purposes of writing the MIME parts.  <a href="https://msdn.microsoft.com/1fa9ecfc-c791-459f-ae11-ffcdc82b7145">WsWriteBytes</a> and
          <a href="https://msdn.microsoft.com/39e25db6-e51f-45cb-9739-260e7c246fcc">WsPullBytes</a> need to buffer data in order to emit the data as a separate MIME part that
          follows the document, and this can be used to limit how much is buffered.
        


          This property defaults to 65536.
        


### -field WS_XML_WRITER_PROPERTY_INITIAL_BUFFER

A <a href="https://msdn.microsoft.com/0106e372-80bf-4a62-b941-1a4501c92a9c">WS_BYTES</a> structure that contains a buffer that the writer may use for encoding the xml document.  This is
          useful when an upper bound on the size of the generated xml data is known, or the caller wants to own
          the buffer in which the bytes are placed.
        


          If the size specified is greater than or equal to <a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_BUFFER_MAX_SIZE</a>, then the 
          writer will not allocate from its internal buffers.
        


        This buffer may appear as one of the buffers returned by the property <a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_BUFFERS</a>
        or <b>WS_XML_WRITER_PROPERTY_BYTES</b>.
        


          The caller must ensure that the buffer specified is valid for the lifetime of the writer.
        


### -field WS_XML_WRITER_PROPERTY_ALLOW_INVALID_CHARACTER_REFERENCES


          A <b>BOOL</b> used with  <a href="https://msdn.microsoft.com/916e693b-9804-4c93-869d-0c3b576e5b61">WS_XML_WRITER_TEXT_ENCODING</a>.  Setting this to <b>TRUE</b> permits character references
          of characters considered invalid by XML 1.0 to be accepted.
        


          Setting this property to <b>TRUE</b> may affect interoperability.
        


          This property defaults to <b>FALSE</b>.
        


### -field WS_XML_WRITER_PROPERTY_MAX_NAMESPACES


          A <b>ULONG</b> that specifies the maximum number of xmlns unique declarations that may appear in scope at any point
          while writing the document.
        


          This property defaults to 32.
        


### -field WS_XML_WRITER_PROPERTY_BYTES_WRITTEN

A <b>ULONG</b> that specifies one of the following.


          If the writer is using <a href="https://msdn.microsoft.com/46c0595c-9aa5-47cf-931a-8dc35e265fa0">WS_XML_WRITER_BUFFER_OUTPUT</a>, then this property
          returns the number of bytes that have been written to the writer.
        


          If the writer is using <a href="https://msdn.microsoft.com/8ee4ea59-5cdc-43bf-80c0-8f8632fee274">WS_XML_WRITER_STREAM_OUTPUT</a>, then this property
          returns the number of bytes that have been written to the writer since the last call to
          <a href="https://msdn.microsoft.com/ba631942-d5a0-4d93-9899-c3f0ebd4aae5">WsFlushWriter</a>.
        


          If the writer is currently writing an element start tag, then the size of the start tag is not included in
          the value returned.
        


          This property is not available on a writer that was set using <a href="https://msdn.microsoft.com/b969700d-7145-45eb-ad4b-c6e643975709">WsSetOutputToBuffer</a>.
        


### -field WS_XML_WRITER_PROPERTY_BYTES_TO_CLOSE


          A <b>ULONG</b> that returns the maximum number of bytes necessary to close any open elements.
        


          An application can use <a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_BYTES_WRITTEN</a> and 
          <b>WS_XML_WRITER_PROPERTY_BYTES_TO_CLOSE</b> to approximate how much additional
          data may be written to the document.  When doing so, the application should take into account
          the encoding of the document being written.
        


          This property is not available on a writer that was set using <a href="https://msdn.microsoft.com/b969700d-7145-45eb-ad4b-c6e643975709">WsSetOutputToBuffer</a>.
        


### -field WS_XML_WRITER_PROPERTY_COMPRESS_EMPTY_ELEMENTS

A <b>BOOL</b>
                that controls how <a href="https://msdn.microsoft.com/36078f7d-4c1f-4b8a-9f44-cd4949b7de04">WsCopyNode</a> copies elements with no content.
            


                When this property is set to <b>FALSE</b>, <a href="https://msdn.microsoft.com/36078f7d-4c1f-4b8a-9f44-cd4949b7de04">WsCopyNode</a>
                    preserves whether each element is represented
                    as a start/end tag pair, or as an empty element.  When this property is set to <b>TRUE</b>, <b>WsCopyNode</b> wlll 
                convert elements with no content to empty elements.
            


                The binary encoding does not support empty elements.  When using <a href="https://msdn.microsoft.com/36078f7d-4c1f-4b8a-9f44-cd4949b7de04">WsCopyNode</a> with
              a writer using the binary encoding this property has no effect either way.  All empty elements are
              converted into elements with no content.
           


                By default, this property is <b>FALSE</b>.
            

For an input XML string like:
            

<pre class="syntax" xml:space="preserve"><code>
&lt;?xml version="1.0" encoding="utf-8"?&gt;
&lt;container&gt;
 &lt;emptyElement /&gt;
 &lt;emptyElementWithEndTag&gt;&lt;/emptyElementWithEndTag&gt;
&lt;/container&gt;</code></pre>
If this property is <b>FALSE</b>,  <a href="https://msdn.microsoft.com/36078f7d-4c1f-4b8a-9f44-cd4949b7de04">WsCopyNode</a>
                will generate the following xml:
                
                    

<pre class="syntax" xml:space="preserve"><code>
&lt;?xml version="1.0" encoding="utf-8"?&gt;
&lt;container&gt;
 &lt;emptyElement /&gt;
 &lt;emptyElementWithEndTag&gt;&lt;/emptyElementWithEndTag&gt;
&lt;/container&gt;</code></pre>

                    If this property is <b>TRUE</b>, <a href="https://msdn.microsoft.com/36078f7d-4c1f-4b8a-9f44-cd4949b7de04">WsCopyNode</a> will generate the following xml:
            

<pre class="syntax" xml:space="preserve"><code>
&lt;?xml version="1.0" encoding="utf-8"?&gt;
&lt;container&gt;
 &lt;emptyElement /&gt;
 &lt;emptyElementWithEndTag /&gt;
&lt;/container&gt;</code></pre>

### -field WS_XML_WRITER_PROPERTY_EMIT_UNCOMPRESSED_EMPTY_ELEMENTS

Windows 8 or later: A <b>BOOL</b> that controls how empty elements are emitted.

If set to <b>FALSE</b>, an element that is created by only calls to <a href="https://msdn.microsoft.com/da23f5e6-504c-4e93-9190-7d8c41efc0da">WsWriteStartElement</a> and <a href="https://msdn.microsoft.com/cfb23857-bc51-4467-9aeb-6ce8810ae1b0">WsWriteEndElement</a> will be emitted as follows:

<pre class="syntax" xml:space="preserve"><code>&lt;emptyElement /&gt;</code></pre>
If set to <b>TRUE</b>, that element will be emitted as follows:

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;emptyElement&gt;&lt;/emptyElement&gt;
</pre>
</td>
</tr>
</table></span></div>
The default is <b>FALSE</b>

