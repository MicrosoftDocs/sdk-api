---
UID: TP:wsw
ms.assetid: dc4e8f4e-add6-3a79-a002-c7682bed67b6
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Windows Web Services



Overview of the Windows Web Services technology.

To develop Windows Web Services, you need these headers:

 * [icontentprefetchertasktrigger.h](..\icontentprefetchertasktrigger\index.md)
 * [webservices.h](..\webservices\index.md)

For the programming guide, see [Windows Web Services](/windows/desktop/wsw).

## Functions

| Title   | Description   |
| ---- |:---- |
| [WsAbandonCall function](..\webservices\nf-webservices-wsabandoncall.md) | Abandons a specified call on the specified service proxy. |
| [WsAbandonMessage function](..\webservices\nf-webservices-wsabandonmessage.md) | Skips the remainder of a specified message on a specified channel. |
| [WsAbortChannel function](..\webservices\nf-webservices-wsabortchannel.md) | Cancels all pending I/O for a specified channel. |
| [WsAbortListener function](..\webservices\nf-webservices-wsabortlistener.md) | Cancels any pending I/O for the specified listener. |
| [WsAbortServiceHost function](..\webservices\nf-webservices-wsabortservicehost.md) | Aborts all current operations on the specified service host. |
| [WsAbortServiceProxy function](..\webservices\nf-webservices-wsabortserviceproxy.md) | Aborts the service proxy, and cancels any pending I/O on the service proxy. |
| [WsAcceptChannel function](..\webservices\nf-webservices-wsacceptchannel.md) | Accepts the next incoming message from the specified listener. |
| [WsAddCustomHeader function](..\webservices\nf-webservices-wsaddcustomheader.md) | Adds the specified application-defined header to the message. |
| [WsAddErrorString function](..\webservices\nf-webservices-wsadderrorstring.md) | Adds a specified error string to the error object. |
| [WsAddMappedHeader function](..\webservices\nf-webservices-wsaddmappedheader.md) | Adds a specified mapped header to the message. |
| [WsAddressMessage function](..\webservices\nf-webservices-wsaddressmessage.md) | Addresses a message to a specified endpoint address. |
| [WsAlloc function](..\webservices\nf-webservices-wsalloc.md) | Allocates a segment of memory from the specified heap. |
| [WsAsyncExecute function](..\webservices\nf-webservices-wsasyncexecute.md) | Helper function for implementing an asynchronous operation. |
| [WsCall function](..\webservices\nf-webservices-wscall.md) | Used internally by the service proxy to format the specified arguments according to the specified metadata and send them in a message. The application should never call this function directly. |
| [WsCheckMustUnderstandHeaders function](..\webservices\nf-webservices-wscheckmustunderstandheaders.md) | Verifies that the specified headers were understood by the receiver. Note  This function should be called after all headers have been read for a received message.  . |
| [WsCloseChannel function](..\webservices\nf-webservices-wsclosechannel.md) | Closes a specified channel. |
| [WsCloseListener function](..\webservices\nf-webservices-wscloselistener.md) | Causes the specified listener to stop listening. |
| [WsCloseServiceHost function](..\webservices\nf-webservices-wscloseservicehost.md) | Closes down communication with the specified service host. |
| [WsCloseServiceProxy function](..\webservices\nf-webservices-wscloseserviceproxy.md) | Closes down communication with the specified service proxy. |
| [WsCombineUrl function](..\webservices\nf-webservices-wscombineurl.md) | Produces an absolute URL from a specified URL reference (absolute or relative URL) and a specified absolute base URL. |
| [WsCopyError function](..\webservices\nf-webservices-wscopyerror.md) | Copies an error object from a specified source to a specifed destination. |
| [WsCopyNode function](..\webservices\nf-webservices-wscopynode.md) | Copies the current node from the specified XML reader to the specified XML writer. |
| [WsCreateChannel function](..\webservices\nf-webservices-wscreatechannel.md) | Creates a channel for message exchange with an endpoint. |
| [WsCreateChannelForListener function](..\webservices\nf-webservices-wscreatechannelforlistener.md) | Creates a channel associated with a specified listener. |
| [WsCreateError function](..\webservices\nf-webservices-wscreateerror.md) | Creates an error object that can passed to functions to record rich error information. |
| [WsCreateFaultFromError function](..\webservices\nf-webservices-wscreatefaultfromerror.md) | Constructs a WS_FAULT from a specified error object. |
| [WsCreateHeap function](..\webservices\nf-webservices-wscreateheap.md) | Creates a heap object. |
| [WsCreateListener function](..\webservices\nf-webservices-wscreatelistener.md) | Creates a listener with the specified properties. |
| [WsCreateMessage function](..\webservices\nf-webservices-wscreatemessage.md) | Creates a message object with the specified properties. |
| [WsCreateMessageForChannel function](..\webservices\nf-webservices-wscreatemessageforchannel.md) | Creates a message for use with a specified channel. |
| [WsCreateMetadata function](..\webservices\nf-webservices-wscreatemetadata.md) | Creates a metadata object that is used to collect and process metadata documents. |
| [WsCreateReader function](..\webservices\nf-webservices-wscreatereader.md) | Creates an XML reader with the specified properties. |
| [WsCreateServiceEndpointFromTemplate function](..\webservices\nf-webservices-wscreateserviceendpointfromtemplate.md) | Helper routine for creating a service endpoint (WS_SERVICE_ENDPOINT) from policy templates. |
| [WsCreateServiceHost function](..\webservices\nf-webservices-wscreateservicehost.md) | Creates a service host for the specified endpoints. |
| [WsCreateServiceProxy function](..\webservices\nf-webservices-wscreateserviceproxy.md) | Creates a service proxy with the specified properties. |
| [WsCreateServiceProxyFromTemplate function](..\webservices\nf-webservices-wscreateserviceproxyfromtemplate.md) | Helper routine for creating a service proxy from policy templates. |
| [WsCreateWriter function](..\webservices\nf-webservices-wscreatewriter.md) | creates an XML Writer with the specified properties. |
| [WsCreateXmlBuffer function](..\webservices\nf-webservices-wscreatexmlbuffer.md) | Creates an XML Buffer which can be used to process XML data . |
| [WsCreateXmlSecurityToken function](..\webservices\nf-webservices-wscreatexmlsecuritytoken.md) | Creates a security token from its specified XML form. |
| [WsDateTimeToFileTime function](..\webservices\nf-webservices-wsdatetimetofiletime.md) | Converts a WS_DATETIME object into a FILETIME object. A reference to the FILETIME object is returned by output parameter. |
| [WsDecodeUrl function](..\webservices\nf-webservices-wsdecodeurl.md) | Evaluates the components of an URL to determine its &#0034;scheme&#0034;. |
| [WsEncodeUrl function](..\webservices\nf-webservices-wsencodeurl.md) | Encodes the specified WS_URL into a URL string given its component parts. Values are escaped as necessary, combined, and stored in the specified WS_HEAP, and the result is returned as a WS_STRING. |
| [WsEndReaderCanonicalization function](..\webservices\nf-webservices-wsendreadercanonicalization.md) | This function stops XML canonicalization started by a preceding WsStartReaderCanonicalization function call. Any remaining canonical bytes buffered by the reader will be written to the callback function. |
| [WsEndWriterCanonicalization function](..\webservices\nf-webservices-wsendwritercanonicalization.md) | This function stops XML canonicalization started by the preceding WsStartWriterCanonicalization call. Remaining canonical bytes buffered by the writer are written to the callback function. |
| [WsFileTimeToDateTime function](..\webservices\nf-webservices-wsfiletimetodatetime.md) | Takes a reference to a FILETIME object and converts it into a WS_DATETIME object. A reference to the WS_DATETIME object is returned by output parameter. |
| [WsFillBody function](..\webservices\nf-webservices-wsfillbody.md) | Ensures that there are a sufficient number of bytes available in a message for reading. |
| [WsFillReader function](..\webservices\nf-webservices-wsfillreader.md) | Ensures that the reader has buffered the minimum byte count of XML data for use by subsequent reader functions. |
| [WsFindAttribute function](..\webservices\nf-webservices-wsfindattribute.md) | Searches the attributes of the current element for an attribute with the specified name and namespace and returns its index which may be passed to WsReadStartAttribute. |
| [WsFlushBody function](..\webservices\nf-webservices-wsflushbody.md) | Flushes all accumulated message body data that has been written. |
| [WsFlushWriter function](..\webservices\nf-webservices-wsflushwriter.md) | Instructs the writer to invoke the callback specified in WS_XML_WRITER_STREAM_OUTPUT if sufficient data has been buffered. |
| [WsFreeChannel function](..\webservices\nf-webservices-wsfreechannel.md) | Releases the memory resource associated with a Channel object. |
| [WsFreeError function](..\webservices\nf-webservices-wsfreeerror.md) | Releases the memory resource associated with an Error object created using WsCreateError. This releases the object and its constituent information. |
| [WsFreeHeap function](..\webservices\nf-webservices-wsfreeheap.md) | This frees the heap object, and the memory associated with any allocations made on it using WsAlloc. |
| [WsFreeListener function](..\webservices\nf-webservices-wsfreelistener.md) | Releases the memory resource associated with a Listener object. |
| [WsFreeMessage function](..\webservices\nf-webservices-wsfreemessage.md) | Releases the memory resource associated with a Message object. |
| [WsFreeMetadata function](..\webservices\nf-webservices-wsfreemetadata.md) | Releases the memory resource associated with a metadata object. |
| [WsFreeReader function](..\webservices\nf-webservices-wsfreereader.md) | Releases the memory resource associated with an XML_Reader object. |
| [WsFreeSecurityToken function](..\webservices\nf-webservices-wsfreesecuritytoken.md) | Releases the memory resource associated with a Security Token object. |
| [WsFreeServiceHost function](..\webservices\nf-webservices-wsfreeservicehost.md) | Releases the memory associated with a Service Host object. |
| [WsFreeServiceProxy function](..\webservices\nf-webservices-wsfreeserviceproxy.md) | Releases the memory associated with a Service Proxy resource. |
| [WsFreeWriter function](..\webservices\nf-webservices-wsfreewriter.md) | Releases the memory resource associated with an XML Writer object. |
| [WsGetChannelProperty function](..\webservices\nf-webservices-wsgetchannelproperty.md) | Retrieves a property of the Channel referenced by the channel parameter. |
| [WsGetCustomHeader function](..\webservices\nf-webservices-wsgetcustomheader.md) | Finds an application-defined header of the message and deserializes it. |
| [WsGetDictionary function](..\webservices\nf-webservices-wsgetdictionary.md) | Retrieves an XML Dictionary object. The retrieved Dictionary is returned by the dictionary reference parameter. |
| [WsGetErrorProperty function](..\webservices\nf-webservices-wsgeterrorproperty.md) | Retrieves a property of an WS_ERROR object referenced by the error parameter. |
| [WsGetErrorString function](..\webservices\nf-webservices-wsgeterrorstring.md) | Retrieves an error string from an error object. |
| [WsGetFaultErrorDetail function](..\webservices\nf-webservices-wsgetfaulterrordetail.md) | Read the fault detail stored in a WS_ERROR object. |
| [WsGetFaultErrorProperty function](..\webservices\nf-webservices-wsgetfaulterrorproperty.md) | Retrieves a Fault error property of an WS_ERROR object referenced by the error parameter. |
| [WsGetHeader function](..\webservices\nf-webservices-wsgetheader.md) | Finds a particular standard header in the message and deserializes it. |
| [WsGetHeaderAttributes function](..\webservices\nf-webservices-wsgetheaderattributes.md) | This function populates a ULONG parameter with the WS_HEADER_ATTRIBUTES from the header element on which the reader is positioned. The envelope version of the message is used to determine which attributes to return. |
| [WsGetHeapProperty function](..\webservices\nf-webservices-wsgetheapproperty.md) | Retrieves a particular property of a specified Heap. |
| [WsGetListenerProperty function](..\webservices\nf-webservices-wsgetlistenerproperty.md) | Retrieves a specified Listener object property. The property to retrieve is identified by a WS_LISTENER_PROPERTY_ID input parameter. |
| [WsGetMappedHeader function](..\webservices\nf-webservices-wsgetmappedheader.md) | Finds a mapped header in the message and deserializes it. |
| [WsGetMessageProperty function](..\webservices\nf-webservices-wsgetmessageproperty.md) | Retrieves a specified Message object property. The property to retrieve is identified by a WS_MESSAGE_PROPERTY_ID input parameter. |
| [WsGetMetadataEndpoints function](..\webservices\nf-webservices-wsgetmetadataendpoints.md) | Returns the &#0034;Endpoints&#0034; defined within the metadata object documents. |
| [WsGetMetadataProperty function](..\webservices\nf-webservices-wsgetmetadataproperty.md) | Retrieves a specified WS_METADATA object property. |
| [WsGetMissingMetadataDocumentAddress function](..\webservices\nf-webservices-wsgetmissingmetadatadocumentaddress.md) | This function returns the address of a missing document that is referenced by the metadata object. |
| [WsGetNamespaceFromPrefix function](..\webservices\nf-webservices-wsgetnamespacefromprefix.md) | This function returns a namespace from the prefix to which it is bound. |
| [WsGetOperationContextProperty function](..\webservices\nf-webservices-wsgetoperationcontextproperty.md) | Returns a property of the specified operation context. It should be noted that the validity of these property is limited to the lifetime of the operation context itself. |
| [WsGetPolicyAlternativeCount function](..\webservices\nf-webservices-wsgetpolicyalternativecount.md) | Retrieves the number of alternatives available in the policy object. |
| [WsGetPolicyProperty function](..\webservices\nf-webservices-wsgetpolicyproperty.md) | Retrieves a property of a policy object. |
| [WsGetPrefixFromNamespace function](..\webservices\nf-webservices-wsgetprefixfromnamespace.md) | This function returns the prefix to which a namespace is bound. |
| [WsGetReaderNode function](..\webservices\nf-webservices-wsgetreadernode.md) | The function returns the XML node at the current position of the XML reader. |
| [WsGetReaderPosition function](..\webservices\nf-webservices-wsgetreaderposition.md) | Returns the current position of the reader. This can only be used on a reader that is set to an XmlBuffer. |
| [WsGetReaderProperty function](..\webservices\nf-webservices-wsgetreaderproperty.md) | This function returns a property of the specified XML Reader.Note  Obtaining the Property WS_XML_READER_PROPERTY_CHARSET will require inspecting up to the first four bytes of the XML data. |
| [WsGetSecurityContextProperty function](..\webservices\nf-webservices-wsgetsecuritycontextproperty.md) | Gets a property of the specified security context. |
| [WsGetSecurityTokenProperty function](..\webservices\nf-webservices-wsgetsecuritytokenproperty.md) | Extracts a field or a property from a security token. |
| [WsGetServiceHostProperty function](..\webservices\nf-webservices-wsgetservicehostproperty.md) | Retrieves a specified Service Host property. The property to retrieve is identified by a WS_SERVICE_PROPERTY_ID input parameter. |
| [WsGetServiceProxyProperty function](..\webservices\nf-webservices-wsgetserviceproxyproperty.md) | This function retrieves a specified Service Proxy property. The property to retrieve is identified by a WS_PROXY_PROPERTY_ID input parameter. |
| [WsGetWriterPosition function](..\webservices\nf-webservices-wsgetwriterposition.md) | Returns the current position of the writer. This can only be used on a writer that is set to an XmlBuffer. When writing to a buffer, the position represents the xml node before which new data will be placed. |
| [WsGetWriterProperty function](..\webservices\nf-webservices-wsgetwriterproperty.md) | Retrieves a specified XML Writer property. The property to retrieve is identified by a WS_XML WRITER_PROPERTY_ID input parameter. |
| [WsGetXmlAttribute function](..\webservices\nf-webservices-wsgetxmlattribute.md) | Finds the nearest xml attribute in scope with the specified localName and returns its value. The returned value is placed on the specified heap. |
| [WsInitializeMessage function](..\webservices\nf-webservices-wsinitializemessage.md) | This function initializes the headers for the message in preparation for processing. |
| [WsMarkHeaderAsUnderstood function](..\webservices\nf-webservices-wsmarkheaderasunderstood.md) | This function marks a header as &#0034;understood&#0034; by the application. |
| [WsMatchPolicyAlternative function](..\webservices\nf-webservices-wsmatchpolicyalternative.md) | Verifies that a Policy Alternative is compatible with the specified Policy Constraint. |
| [WsMoveReader function](..\webservices\nf-webservices-wsmovereader.md) | Moves the current position of the reader as specified by the moveTo parameter. This function can only be used on a reader that is set to an XmlBuffer. |
| [WsMoveWriter function](..\webservices\nf-webservices-wsmovewriter.md) | Moves the current position of the writer as specified by the moveTo parameter. |
| [WsOpenChannel function](..\webservices\nf-webservices-wsopenchannel.md) | Open a channel to an endpoint. |
| [WsOpenListener function](..\webservices\nf-webservices-wsopenlistener.md) | Initiates &#0034;listening&#0034; on a specified address. Once a listener is opened channels can be accepted from it. If the open is successful the Listener must be closed using the WsCloseListener function before Listener resources can be released. |
| [WsOpenServiceHost function](..\webservices\nf-webservices-wsopenservicehost.md) | Opens a Service Host for communication and starts the Listeners on all the endpoints. Client applications cannot connect to Service endpoints until WsOpenSerivceHost is called. |
| [WsOpenServiceProxy function](..\webservices\nf-webservices-wsopenserviceproxy.md) | Opens a Service Proxy to a Service endpoint. On success client applications can make calls using the Service Proxy. The behavior of WsOpenServiceProxy is governed by the channel binding used. |
| [WsPullBytes function](..\webservices\nf-webservices-wspullbytes.md) | Sets up a callback to be invoked to obtain the bytes to be written within an element. In some encodings this can be more efficient by eliminating a copy of the data. |
| [WsPushBytes function](..\webservices\nf-webservices-wspushbytes.md) | Establishes a callback to be invoked to write bytes within an element. In some encodings this can be more efficient by eliminating a copy of the data. |
| [WsReadArray function](..\webservices\nf-webservices-wsreadarray.md) | Reads a series of elements from the reader and interprets their content according to the specified value type. |
| [WsReadAttribute function](..\webservices\nf-webservices-wsreadattribute.md) | Read an attribute producing a value of the specified WS_TYPE. |
| [WsReadBody function](..\webservices\nf-webservices-wsreadbody.md) | This is a helper function that deserializes a value from the XML Reader of the message. The WS_MESSAGE_STATE must be set to WS_MESSAGE_STATE_READING. This function does not cause any state transitions. |
| [WsReadBytes function](..\webservices\nf-webservices-wsreadbytes.md) | Reads text from the Reader and decodes the characters as bytes according to the base64 specification. |
| [WsReadChars function](..\webservices\nf-webservices-wsreadchars.md) | Reads a specified number of text characters from the Reader. |
| [WsReadCharsUtf8 function](..\webservices\nf-webservices-wsreadcharsutf8.md) | Reads a specified number of text characters from the reader and returns them encoded in UTF-8. |
| [WsReadElement function](..\webservices\nf-webservices-wsreadelement.md) | Read an element producing a value of the specified WS_TYPE. |
| [WsReadEndAttribute function](..\webservices\nf-webservices-wsreadendattribute.md) | Moves the reader back to the element node containing the attribute that was read. |
| [WsReadEndElement function](..\webservices\nf-webservices-wsreadendelement.md) | This function ensures that the current Reader node is an End element and advances the reader to the next node. |
| [WsReadEndpointAddressExtension function](..\webservices\nf-webservices-wsreadendpointaddressextension.md) | Reads an extension of the WS_ENDPOINT_ADDRESS. |
| [WsReadEnvelopeEnd function](..\webservices\nf-webservices-wsreadenvelopeend.md) | Reads the closing elements of a message. The operation allows for reading of messages from sources other than Channels. If the source is a Channel use WsReadMessageEnd. |
| [WsReadEnvelopeStart function](..\webservices\nf-webservices-wsreadenvelopestart.md) | Reads the headers of the message and prepare to read the body elements. |
| [WsReadMessageEnd function](..\webservices\nf-webservices-wsreadmessageend.md) | Read the closing elements of a message from a channel. |
| [WsReadMessageStart function](..\webservices\nf-webservices-wsreadmessagestart.md) | Read the headers of the next message from the channel, and prepare to read the body elements. |
| [WsReadMetadata function](..\webservices\nf-webservices-wsreadmetadata.md) | Reads a Metadata element and adds it to the Metadata documents of the Metadata object. |
| [WsReadNode function](..\webservices\nf-webservices-wsreadnode.md) | This operation advances the Reader to the next node in the input stream. |
| [WsReadQualifiedName function](..\webservices\nf-webservices-wsreadqualifiedname.md) | Reads a qualified name and separates it into its prefix, localName and namespace based on the current namespace scope of the XML_READER. |
| [WsReadStartAttribute function](..\webservices\nf-webservices-wsreadstartattribute.md) | Moves the Reader to the specified attribute so that the content may be read using WsReadValue, WsReadChars, or WsReadBytes. |
| [WsReadStartElement function](..\webservices\nf-webservices-wsreadstartelement.md) | Calling this function advances the reader past a start element skipping any whitespace. |
| [WsReadToStartElement function](..\webservices\nf-webservices-wsreadtostartelement.md) | Advances the reader to the next start element skipping whitespace and comments if necessary. Optionally, it may also verify the localName and namespace of the element. |
| [WsReadType function](..\webservices\nf-webservices-wsreadtype.md) | Read a value of a given WS_TYPE from XML according to the WS_TYPE_MAPPING. |
| [WsReadValue function](..\webservices\nf-webservices-wsreadvalue.md) | Reads text from a Reader and parses it according to the specified value type. |
| [WsReadXmlBuffer function](..\webservices\nf-webservices-wsreadxmlbuffer.md) | Reads the current node from a reader into a WS_XML_BUFFER. |
| [WsReadXmlBufferFromBytes function](..\webservices\nf-webservices-wsreadxmlbufferfrombytes.md) | Uses a reader to convert a set of encoded bytes to a WS_XML_BUFFER. |
| [WsReceiveMessage function](..\webservices\nf-webservices-wsreceivemessage.md) | Receive a message and deserialize the body of the message as a value. |
| [WsRegisterOperationForCancel function](..\webservices\nf-webservices-wsregisteroperationforcancel.md) | A service operation can use this function to register for a cancel notification. |
| [WsRemoveCustomHeader function](..\webservices\nf-webservices-wsremovecustomheader.md) | Removes a custom header from the message. This function is designed to handle types of headers that appear once in the message and are targeted at the ultimate receiver. Headers targeted with a role other than ultimate receiver are ignored. |
| [WsRemoveHeader function](..\webservices\nf-webservices-wsremoveheader.md) | Removes the standard WS_HEADER_TYPE object from a message. |
| [WsRemoveMappedHeader function](..\webservices\nf-webservices-wsremovemappedheader.md) | Removes all instances of a mapped header from the message. |
| [WsRemoveNode function](..\webservices\nf-webservices-wsremovenode.md) | Removes the node at the specified position from the xml buffer. |
| [WsRequestReply function](..\webservices\nf-webservices-wsrequestreply.md) | Used to send a request message and receive a correlated reply message. |
| [WsRequestSecurityToken function](..\webservices\nf-webservices-wsrequestsecuritytoken.md) | Get a security token from a security token service (STS) that acts as the token issuer in a federation scenario. |
| [WsResetChannel function](..\webservices\nf-webservices-wsresetchannel.md) | Reset a channel so it can be reused. |
| [WsResetError function](..\webservices\nf-webservices-wsreseterror.md) | Releases the content of the error object parameter but does not release the resource allocated to the error object parameter. |
| [WsResetHeap function](..\webservices\nf-webservices-wsresetheap.md) | Releases all Heap allocations. Allocations made on the Heap using WsAlloc are no longer valid. Allocation for the Heap object itself is not released. |
| [WsResetListener function](..\webservices\nf-webservices-wsresetlistener.md) | Resets a Listener object so it can be reused. Use of this function requires that the Listener state be set to WS_LISTENER_STATE_CREATED or WS_LISTENER_STATE_CLOSED. |
| [WsResetMessage function](..\webservices\nf-webservices-wsresetmessage.md) | Sets the Message state back to WS_MESSAGE_STATE_EMPTY. In this state the Message object can be reused. |
| [WsResetMetadata function](..\webservices\nf-webservices-wsresetmetadata.md) | Resets a metadata object state to WS_METADATA_STATE_CREATED. In this state the Metadata object can be reused. WS_POLICY objects that were retrieved using the Metadata object will be released. |
| [WsResetServiceHost function](..\webservices\nf-webservices-wsresetservicehost.md) | Resets service host so that it can be opened again. |
| [WsResetServiceProxy function](..\webservices\nf-webservices-wsresetserviceproxy.md) | Resets service proxy. |
| [WsRevokeSecurityContext function](..\webservices\nf-webservices-wsrevokesecuritycontext.md) | Revokes a security context. |
| [WsSendFaultMessageForError function](..\webservices\nf-webservices-wssendfaultmessageforerror.md) | Sends a fault message given a WS_ERROR object. |
| [WsSendMessage function](..\webservices\nf-webservices-wssendmessage.md) | Send a message on a channel using serialization to write the body element. |
| [WsSendReplyMessage function](..\webservices\nf-webservices-wssendreplymessage.md) | Sends a message which is a reply to a received message. |
| [WsSetChannelProperty function](..\webservices\nf-webservices-wssetchannelproperty.md) | Sets a property of the channel. |
| [WsSetErrorProperty function](..\webservices\nf-webservices-wsseterrorproperty.md) | Sets an WS_ERROR object property. |
| [WsSetFaultErrorDetail function](..\webservices\nf-webservices-wssetfaulterrordetail.md) | Write the fault detail stored in a WS_ERROR object. |
| [WsSetFaultErrorProperty function](..\webservices\nf-webservices-wssetfaulterrorproperty.md) | Set a Fault property of a WS_ERROR object. |
| [WsSetHeader function](..\webservices\nf-webservices-wssetheader.md) | Adds or replaces the specified standard header in the message. |
| [WsSetInput function](..\webservices\nf-webservices-wssetinput.md) | Sets the encoding and input sources for an XML Reader. |
| [WsSetInputToBuffer function](..\webservices\nf-webservices-wssetinputtobuffer.md) | Sets Reader input to a specified XML buffer. Reader properties specified to WsSetInputToBuffer override properties set by WsCreateReader. |
| [WsSetListenerProperty function](..\webservices\nf-webservices-wssetlistenerproperty.md) | Sets a Listenerobject property. |
| [WsSetMessageProperty function](..\webservices\nf-webservices-wssetmessageproperty.md) | This operation sets a Messageproperty. |
| [WsSetOutput function](..\webservices\nf-webservices-wssetoutput.md) | Sets the encoding and output callbacks for the writer. The callbacks are used to provides buffers to the writer and to perform asynchronous i/o. |
| [WsSetOutputToBuffer function](..\webservices\nf-webservices-wssetoutputtobuffer.md) | This operation positions the Writer at the end of the specified buffer. |
| [WsSetReaderPosition function](..\webservices\nf-webservices-wssetreaderposition.md) | Sets the current position of the Reader. The position must have been obtained by a call to WsGetReaderPosition or WsGetWriterPosition. This function can only be used on a reader that is set to a WS_XML_BUFFER. |
| [WsSetWriterPosition function](..\webservices\nf-webservices-wssetwriterposition.md) | Sets the current position of the writer. The position must have been obtained by a call to WsGetReaderPosition or WsGetWriterPosition. |
| [WsShutdownSessionChannel function](..\webservices\nf-webservices-wsshutdownsessionchannel.md) | Used to signal the end of messages for a session channel. |
| [WsSkipNode function](..\webservices\nf-webservices-wsskipnode.md) | Advances the reader in the input stream. |
| [WsStartReaderCanonicalization function](..\webservices\nf-webservices-wsstartreadercanonicalization.md) | This operation begins the process of putting the specified XML Reader in a standard or &#0034;canonized&#0034; form. |
| [WsStartWriterCanonicalization function](..\webservices\nf-webservices-wsstartwritercanonicalization.md) | Starts canonicalization on the specified XML writer. |
| [WsTrimXmlWhitespace function](..\webservices\nf-webservices-wstrimxmlwhitespace.md) | Removes leading and trailing whitespace from a sequence of characters. |
| [WsVerifyXmlNCName function](..\webservices\nf-webservices-wsverifyxmlncname.md) | Verifies whether the input string is a valid XML NCName. |
| [WsWriteArray function](..\webservices\nf-webservices-wswritearray.md) | This operation sends a series of elements to an XML Writer. |
| [WsWriteAttribute function](..\webservices\nf-webservices-wswriteattribute.md) | Write a typed value as an XML attribute. |
| [WsWriteBody function](..\webservices\nf-webservices-wswritebody.md) | Writes a value in the body of a message. This is a helper function that serializes a value to the XML Writer of the message. The message state must be set to WS_MESSAGE_STATE_WRITING. This function does not cause any state transitions. |
| [WsWriteBytes function](..\webservices\nf-webservices-wswritebytes.md) | Writes bytes to the writer in a format optimized for the encoding. When writing in a text encoding, it will emit the bytes encoded in base64. When writing to a binary format, it will emit the bytes directly. |
| [WsWriteChars function](..\webservices\nf-webservices-wswritechars.md) | Writes a series of characters to an element or attribute. |
| [WsWriteCharsUtf8 function](..\webservices\nf-webservices-wswritecharsutf8.md) | Writes a series of characters encoded as UTF-8 to an element or attribute. |
| [WsWriteElement function](..\webservices\nf-webservices-wswriteelement.md) | Write a typed value as an XML element. |
| [WsWriteEndAttribute function](..\webservices\nf-webservices-wswriteendattribute.md) | This operation finishes writing an attribute to the current element. If WsWriteStartAttribute is called the Writer does not permit another element or attribute to be written until WsWriteEndAttribute is called. |
| [WsWriteEndCData function](..\webservices\nf-webservices-wswriteendcdata.md) | Ends a CDATA section in the writer. |
| [WsWriteEndElement function](..\webservices\nf-webservices-wswriteendelement.md) | Writes an end element to a Writer. |
| [WsWriteEndStartElement function](..\webservices\nf-webservices-wswriteendstartelement.md) | Forces the writer to commit the current element and prevent further attributes from being written to the element. |
| [WsWriteEnvelopeEnd function](..\webservices\nf-webservices-wswriteenvelopeend.md) | Writes the closing elements of a message. |
| [WsWriteEnvelopeStart function](..\webservices\nf-webservices-wswriteenvelopestart.md) | Writes the start of the message including the current set of headers of the message and prepares to write the body elementss. |
| [WsWriteMessageEnd function](..\webservices\nf-webservices-wswritemessageend.md) | Write the closing elements of the message to the channel. |
| [WsWriteMessageStart function](..\webservices\nf-webservices-wswritemessagestart.md) | Write out all the headers of the message to the channel, and prepare to write the body elements. |
| [WsWriteNode function](..\webservices\nf-webservices-wswritenode.md) | Writes the specified node to the XML Writer. |
| [WsWriteQualifiedName function](..\webservices\nf-webservices-wswritequalifiedname.md) | Writes an XML qualified name to the Writer. |
| [WsWriteStartAttribute function](..\webservices\nf-webservices-wswritestartattribute.md) | This operation starts writing an attribute to the current element. |
| [WsWriteStartCData function](..\webservices\nf-webservices-wswritestartcdata.md) | This operation starts a CDATA section in the writer. |
| [WsWriteStartElement function](..\webservices\nf-webservices-wswritestartelement.md) | Writes a start element to the writer. |
| [WsWriteText function](..\webservices\nf-webservices-wswritetext.md) | Writes the specified text to the XML writer. |
| [WsWriteType function](..\webservices\nf-webservices-wswritetype.md) | Write a value of a given WS_TYPE to XML according to the WS_TYPE_MAPPING. |
| [WsWriteValue function](..\webservices\nf-webservices-wswritevalue.md) | This operation derives the best representation for a primitive value from the underlying encoding and passes the derived value to a Writer object. |
| [WsWriteXmlBuffer function](..\webservices\nf-webservices-wswritexmlbuffer.md) | Writes a WS_XML_BUFFER to a writer. |
| [WsWriteXmlBufferToBytes function](..\webservices\nf-webservices-wswritexmlbuffertobytes.md) | Uses a writer to convert a WS_XML_BUFFER to an encoded set of bytes. |
| [WsWriteXmlnsAttribute function](..\webservices\nf-webservices-wswritexmlnsattribute.md) | Writes an Xmlns attribute to the current element. |
| [WsXmlStringEquals function](..\webservices\nf-webservices-wsxmlstringequals.md) | Compares two WS_XML_STRING objects for equality. The operation performs an ordinal comparison of the character values contained by the String objects. |

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [WS_ABANDON_MESSAGE_CALLBACK callback function](..\webservices\nc-webservices-ws_abandon_message_callback.md) | Handles the WsAbandonMessage call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_ABORT_CHANNEL_CALLBACK callback function](..\webservices\nc-webservices-ws_abort_channel_callback.md) | Handles the WsAbortChannel call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_ABORT_LISTENER_CALLBACK callback function](..\webservices\nc-webservices-ws_abort_listener_callback.md) | Handles the WsAbortListener call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_ACCEPT_CHANNEL_CALLBACK callback function](..\webservices\nc-webservices-ws_accept_channel_callback.md) | Handles the WsAcceptChannel call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_ASYNC_CALLBACK callback function](..\webservices\nc-webservices-ws_async_callback.md) | The callback function parameter used with the asynchronous model. |
| [WS_ASYNC_FUNCTION callback function](..\webservices\nc-webservices-ws_async_function.md) | Used with the WsAsyncExecute to specify the next function to invoke in a series of async operations. |
| [WS_CERTIFICATE_VALIDATION_CALLBACK callback function](..\webservices\nc-webservices-ws_certificate_validation_callback.md) | The WS_CERTIFICATE_VALIDATION_CALLBACK callback is invoked to validate a certificate when a connection to an HTTP server has been established and headers sent. |
| [WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK callback function](..\webservices\nc-webservices-ws_cert_issuer_list_notification_callback.md) | Notifies the client of the list of certificate issuers that are acceptable to the server. |
| [WS_CLOSE_CHANNEL_CALLBACK callback function](..\webservices\nc-webservices-ws_close_channel_callback.md) | Handles the WsCloseChannel call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_CLOSE_LISTENER_CALLBACK callback function](..\webservices\nc-webservices-ws_close_listener_callback.md) | Handles the WsCloseListener call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_CREATE_CHANNEL_CALLBACK callback function](..\webservices\nc-webservices-ws_create_channel_callback.md) | Handles the WsCreateChannel call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_CREATE_CHANNEL_FOR_LISTENER_CALLBACK callback function](..\webservices\nc-webservices-ws_create_channel_for_listener_callback.md) | Handles the WsCreateChannelForListener call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_CREATE_DECODER_CALLBACK callback function](..\webservices\nc-webservices-ws_create_decoder_callback.md) | Handles creating an decoder instance. |
| [WS_CREATE_ENCODER_CALLBACK callback function](..\webservices\nc-webservices-ws_create_encoder_callback.md) | Handles creating an encoder instance. |
| [WS_CREATE_LISTENER_CALLBACK callback function](..\webservices\nc-webservices-ws_create_listener_callback.md) | Handles the WsCreateListener call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_DECODER_DECODE_CALLBACK callback function](..\webservices\nc-webservices-ws_decoder_decode_callback.md) | Decodes a message. |
| [WS_DECODER_END_CALLBACK callback function](..\webservices\nc-webservices-ws_decoder_end_callback.md) | Decodes the end of a message. |
| [WS_DECODER_GET_CONTENT_TYPE_CALLBACK callback function](..\webservices\nc-webservices-ws_decoder_get_content_type_callback.md) | Gets the content type of the message. |
| [WS_DECODER_START_CALLBACK callback function](..\webservices\nc-webservices-ws_decoder_start_callback.md) | Starts decoding a message. |
| [WS_DURATION_COMPARISON_CALLBACK callback function](..\webservices\nc-webservices-ws_duration_comparison_callback.md) | Compares two durations. |
| [WS_DYNAMIC_STRING_CALLBACK callback function](..\webservices\nc-webservices-ws_dynamic_string_callback.md) | Determines whether the specified string can be written in optimized form. |
| [WS_ENCODER_ENCODE_CALLBACK callback function](..\webservices\nc-webservices-ws_encoder_encode_callback.md) | Encodes a message. |
| [WS_ENCODER_END_CALLBACK callback function](..\webservices\nc-webservices-ws_encoder_end_callback.md) | Encodes the end of a message. |
| [WS_ENCODER_GET_CONTENT_TYPE_CALLBACK callback function](..\webservices\nc-webservices-ws_encoder_get_content_type_callback.md) | Gets the content type of the message. |
| [WS_ENCODER_START_CALLBACK callback function](..\webservices\nc-webservices-ws_encoder_start_callback.md) | Starts encoding a message. |
| [WS_FREE_CHANNEL_CALLBACK callback function](..\webservices\nc-webservices-ws_free_channel_callback.md) | Handles the WsFreeChannel call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_FREE_DECODER_CALLBACK callback function](..\webservices\nc-webservices-ws_free_decoder_callback.md) | Handles freeing a decoder instance. |
| [WS_FREE_ENCODER_CALLBACK callback function](..\webservices\nc-webservices-ws_free_encoder_callback.md) | Handles freeing an encoder instance. |
| [WS_FREE_LISTENER_CALLBACK callback function](..\webservices\nc-webservices-ws_free_listener_callback.md) | Handles the WsFreeListener call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_GET_CERT_CALLBACK callback function](..\webservices\nc-webservices-ws_get_cert_callback.md) | Provides a certificate to the security runtime. |
| [WS_GET_CHANNEL_PROPERTY_CALLBACK callback function](..\webservices\nc-webservices-ws_get_channel_property_callback.md) | Handles the WsGetChannelProperty call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_GET_LISTENER_PROPERTY_CALLBACK callback function](..\webservices\nc-webservices-ws_get_listener_property_callback.md) | Handles the WsGetListenerProperty call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_HTTP_REDIRECT_CALLBACK callback function](..\webservices\nc-webservices-ws_http_redirect_callback.md) | Invoked when a message is about to be automatically redirected to another service utilizing HTTP auto redirect functionality as described in RFC2616. |
| [WS_IS_DEFAULT_VALUE_CALLBACK callback function](..\webservices\nc-webservices-ws_is_default_value_callback.md) | Determines if a value is the default value. |
| [WS_MESSAGE_DONE_CALLBACK callback function](..\webservices\nc-webservices-ws_message_done_callback.md) | Notifies the caller that the message has completed its use of either the WS_XML_READER structure that was supplied to WsReadEnvelopeStart function, or of the WS_XML_WRITER structure supplied to the WsWriteEnvelopeStart function. |
| [WS_OPEN_CHANNEL_CALLBACK callback function](..\webservices\nc-webservices-ws_open_channel_callback.md) | Handles the WsOpenChannel call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_OPEN_LISTENER_CALLBACK callback function](..\webservices\nc-webservices-ws_open_listener_callback.md) | Handles the WsOpenListener call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_OPERATION_CANCEL_CALLBACK callback function](..\webservices\nc-webservices-ws_operation_cancel_callback.md) | Gives notification of the cancellation of an asynchronous service operation call as a result of an aborted shutdown of service host. |
| [WS_OPERATION_FREE_STATE_CALLBACK callback function](..\webservices\nc-webservices-ws_operation_free_state_callback.md) | Allows an application to cleanup state information that was registered with cancellation callback. |
| [WS_PROXY_MESSAGE_CALLBACK callback function](..\webservices\nc-webservices-ws_proxy_message_callback.md) | Invoked when the headers of the input message are about to be sent, or when output message headers are just received. |
| [WS_PULL_BYTES_CALLBACK callback function](..\webservices\nc-webservices-ws_pull_bytes_callback.md) | Used by the WsPullBytes function to request the data that should be written. |
| [WS_PUSH_BYTES_CALLBACK callback function](..\webservices\nc-webservices-ws_push_bytes_callback.md) | Used by the WsPushBytes function to request that data be written. |
| [WS_READ_CALLBACK callback function](..\webservices\nc-webservices-ws_read_callback.md) | Used by the WS_XML_READER to read from some source into a buffer. |
| [WS_READ_MESSAGE_END_CALLBACK callback function](..\webservices\nc-webservices-ws_read_message_end_callback.md) | Handles the WsReadMessageEnd call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_READ_MESSAGE_START_CALLBACK callback function](..\webservices\nc-webservices-ws_read_message_start_callback.md) | Handles the WsReadMessageStart call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_READ_TYPE_CALLBACK callback function](..\webservices\nc-webservices-ws_read_type_callback.md) | Reads a value when WS_TYPE has been specified. |
| [WS_RESET_CHANNEL_CALLBACK callback function](..\webservices\nc-webservices-ws_reset_channel_callback.md) | Handles the WsResetChannel call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_RESET_LISTENER_CALLBACK callback function](..\webservices\nc-webservices-ws_reset_listener_callback.md) | Handles the WsResetListener call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_SERVICE_ACCEPT_CHANNEL_CALLBACK callback function](..\webservices\nc-webservices-ws_service_accept_channel_callback.md) | Invoked when a channel is accepted on an endpoint listener by service host. |
| [WS_SERVICE_CLOSE_CHANNEL_CALLBACK callback function](..\webservices\nc-webservices-ws_service_close_channel_callback.md) | Invoked when a channel is closed or aborted on an endpoint. |
| [WS_SERVICE_MESSAGE_RECEIVE_CALLBACK callback function](..\webservices\nc-webservices-ws_service_message_receive_callback.md) | Invoked when a WS_MESSAGE is received on an endpoint configured with a WS_SERVICE_CONTRACT which has defaultMessageHandlerCallback set. |
| [WS_SERVICE_SECURITY_CALLBACK callback function](..\webservices\nc-webservices-ws_service_security_callback.md) | Invoked when headers of the incoming message are received and the body is not processed. |
| [WS_SERVICE_STUB_CALLBACK callback function](..\webservices\nc-webservices-ws_service_stub_callback.md) | Invoked by service model to delegate to the service operation call. |
| [WS_SET_CHANNEL_PROPERTY_CALLBACK callback function](..\webservices\nc-webservices-ws_set_channel_property_callback.md) | Handles the WsSetChannelProperty call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_SET_LISTENER_PROPERTY_CALLBACK callback function](..\webservices\nc-webservices-ws_set_listener_property_callback.md) | Handles the WsSetListenerProperty call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK callback function](..\webservices\nc-webservices-ws_shutdown_session_channel_callback.md) | Handles the WsShutdownSessionChannel call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_VALIDATE_PASSWORD_CALLBACK callback function](..\webservices\nc-webservices-ws_validate_password_callback.md) | Validates a username/password pair on the receiver side. |
| [WS_VALIDATE_SAML_CALLBACK callback function](..\webservices\nc-webservices-ws_validate_saml_callback.md) | Validates a SAML assertion. |
| [WS_WRITE_CALLBACK callback function](..\webservices\nc-webservices-ws_write_callback.md) | Used by the WS_XML_WRITER function to write a specified buffer to a user-determined destination. |
| [WS_WRITE_MESSAGE_END_CALLBACK callback function](..\webservices\nc-webservices-ws_write_message_end_callback.md) | Handles the WsWriteMessageEnd call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_WRITE_MESSAGE_START_CALLBACK callback function](..\webservices\nc-webservices-ws_write_message_start_callback.md) | Handles the WsWriteMessageStart call for a WS_CUSTOM_CHANNEL_BINDING. |
| [WS_WRITE_TYPE_CALLBACK callback function](..\webservices\nc-webservices-ws_write_type_callback.md) | Invoked to write an element when WS_CUSTOM_TYPE has been specified. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_WS_ANY_ATTRIBUTE structure](..\webservices\ns-webservices-_ws_any_attribute.md) | This type is used to store an attribute that has not been directly mapped to a field. |
| [_WS_ANY_ATTRIBUTES structure](..\webservices\ns-webservices-_ws_any_attributes.md) | This type is used to store a set of attributes that have not been directly mapped to field of a structure. |
| [_WS_ASYNC_CONTEXT structure](..\webservices\ns-webservices-_ws_async_context.md) | Used with the Async Model to specify the asynchronous callback and a pointer which will be passed to the asynchronous callback. |
| [_WS_ASYNC_OPERATION structure](..\webservices\ns-webservices-_ws_async_operation.md) | Used with the WsAsyncExecute to specify the next function to invoke in a series of async operations. |
| [_WS_ASYNC_STATE structure](..\webservices\ns-webservices-_ws_async_state.md) | Used by WsAsyncExecute to manage the state of an asynchronous operation. |
| [_WS_ATTRIBUTE_DESCRIPTION structure](..\webservices\ns-webservices-_ws_attribute_description.md) | Represents a mapping between a C data type and an XML attribute. |
| [_WS_BOOL_DESCRIPTION structure](..\webservices\ns-webservices-_ws_bool_description.md) | Specifies constraints on the set of values which can be deserialized. |
| [_WS_BUFFERS structure](..\webservices\ns-webservices-_ws_buffers.md) | A structure used to represent a discontiguous array of WS_BYTES. |
| [_WS_BYTES structure](..\webservices\ns-webservices-_ws_bytes.md) | Used to serialize and deserialize an array of bytes. |
| [_WS_BYTES_DESCRIPTION structure](..\webservices\ns-webservices-_ws_bytes_description.md) | Specifies constraints on the set of values which can be deserialized. |
| [_WS_BYTE_ARRAY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_byte_array_description.md) | Specifies constraints on the set of values which can be deserialized. |
| [_WS_CALL_PROPERTY structure](..\webservices\ns-webservices-_ws_call_property.md) | Specifies a proxy property. |
| [_WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE structure](..\webservices\ns-webservices-_ws_capi_asymmetric_security_key_handle.md) | The type for specifying asymmetric cryptographic keys as CAPI 1.0 key handles. |
| [_WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT structure](..\webservices\ns-webservices-_ws_certificate_validation_callback_context.md) | The WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT structure contains the callback function and state for validating the certificate for an HTTP connection. |
| [_WS_CERT_CREDENTIAL structure](..\webservices\ns-webservices-_ws_cert_credential.md) | The abstract base type for all certificate credential types. |
| [_WS_CERT_ENDPOINT_IDENTITY structure](..\webservices\ns-webservices-_ws_cert_endpoint_identity.md) | Type for certificate endpoint identity |
| [_WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT structure](..\webservices\ns-webservices-_ws_cert_message_security_binding_constraint.md) | A security binding constraint that can be used with WS_XML_TOKEN_MESSAGE_SECURITY_BINDING. |
| [_WS_CERT_SIGNED_SAML_AUTHENTICATOR structure](..\webservices\ns-webservices-_ws_cert_signed_saml_authenticator.md) | The type for specifying a SAML token authenticator based on an array of expected issuer certificates. |
| [_WS_CHANNEL_DECODER structure](..\webservices\ns-webservices-_ws_channel_decoder.md) | A structure that is used to specify a set of callbacks that can transform the content type and encoded bytes of a received message. |
| [_WS_CHANNEL_ENCODER structure](..\webservices\ns-webservices-_ws_channel_encoder.md) | A structure that is used to specify a set of callbacks that can transform the content type and encoded bytes of a sent message. |
| [_WS_CHANNEL_PROPERTIES structure](..\webservices\ns-webservices-_ws_channel_properties.md) | Specifies a set of WS_CHANNEL_PROPERTY structures. |
| [_WS_CHANNEL_PROPERTY structure](..\webservices\ns-webservices-_ws_channel_property.md) | Specifies a channel specific setting. |
| [_WS_CHANNEL_PROPERTY_CONSTRAINT structure](..\webservices\ns-webservices-_ws_channel_property_constraint.md) | Specifies constraints for a particular channel property. |
| [_WS_CHAR_ARRAY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_char_array_description.md) | Specifies constraints on the set of values which can be deserialized. |
| [_WS_CONTRACT_DESCRIPTION structure](..\webservices\ns-webservices-_ws_contract_description.md) | The metadata for a service contract for service model. |
| [_WS_CUSTOM_CERT_CREDENTIAL structure](..\webservices\ns-webservices-_ws_custom_cert_credential.md) | The type for specifying a certificate credential that is to be supplied by a callback to the application. |
| [_WS_CUSTOM_CHANNEL_CALLBACKS structure](..\webservices\ns-webservices-_ws_custom_channel_callbacks.md) | A structure that is used to specify a set of callbacks that form the implementation of a custom channel. |
| [_WS_CUSTOM_HTTP_PROXY structure](..\webservices\ns-webservices-_ws_custom_http_proxy.md) | A structure that is used to specify the custom proxy for the channel, using the WS_CHANNEL_PROPERTY_CUSTOM_HTTP_PROXY. |
| [_WS_CUSTOM_LISTENER_CALLBACKS structure](..\webservices\ns-webservices-_ws_custom_listener_callbacks.md) | A structure that is used to specify a set of callbacks that form the implementation of a custom listener. |
| [_WS_CUSTOM_TYPE_DESCRIPTION structure](..\webservices\ns-webservices-_ws_custom_type_description.md) | Represents a custom mapping between a C data type and an XML element. |
| [_WS_DATETIME structure](..\webservices\ns-webservices-_ws_datetime.md) | This structure is used to represent dates and times. |
| [_WS_DATETIME_DESCRIPTION structure](..\webservices\ns-webservices-_ws_datetime_description.md) | This type description is used with WS_DATETIME_TYPE and is optional. It is used to specify constraints on the set of values which can be deserialized. Only the ticks member of the WS_DATETIME is compared. |
| [_WS_DECIMAL_DESCRIPTION structure](..\webservices\ns-webservices-_ws_decimal_description.md) | An optional type description used with WS_DECIMAL_TYPE. It is used to specify constraints on the set of values which can be deserialized. |
| [_WS_DEFAULT_VALUE structure](..\webservices\ns-webservices-_ws_default_value.md) | Defines a default value for a field. This is used in a WS_FIELD_DESCRIPTION. |
| [_WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure](..\webservices\ns-webservices-_ws_default_windows_integrated_auth_credential.md) | Type for supplying a Windows Integrated Authentication credential based on the current Windows identity. |
| [_WS_DISALLOWED_USER_AGENT_SUBSTRINGS structure](..\webservices\ns-webservices-_ws_disallowed_user_agent_substrings.md) | Specifies the list of blocked UserAgent sub-string's. This is used with the WS_LISTENER_PROPERTY_DISALLOWED_USER_AGENT listener property. |
| [_WS_DNS_ENDPOINT_IDENTITY structure](..\webservices\ns-webservices-_ws_dns_endpoint_identity.md) | Type for specifying an endpoint identity represented by a DNS name. |
| [_WS_DOUBLE_DESCRIPTION structure](..\webservices\ns-webservices-_ws_double_description.md) | An optional type description used with WS_DOUBLE_TYPE. It is used to specify constraints on the set of values which can be deserialized. |
| [_WS_DURATION structure](..\webservices\ns-webservices-_ws_duration.md) | Represents a xsd |
| [_WS_DURATION_DESCRIPTION structure](..\webservices\ns-webservices-_ws_duration_description.md) | An optional type description used with WS_DURATION_TYPE. It is used to specify constraints on the set of values which can be deserialized. |
| [_WS_ELEMENT_DESCRIPTION structure](..\webservices\ns-webservices-_ws_element_description.md) | Represents a mapping between a C data type and an XML element. |
| [_WS_ENDPOINT_ADDRESS structure](..\webservices\ns-webservices-_ws_endpoint_address.md) | Represents the network address of an endpoint. |
| [_WS_ENDPOINT_ADDRESS_DESCRIPTION structure](..\webservices\ns-webservices-_ws_endpoint_address_description.md) | Information about a mapping between an WS_ENDPOINT_ADDRESS and an XML element. |
| [_WS_ENDPOINT_IDENTITY structure](..\webservices\ns-webservices-_ws_endpoint_identity.md) | The base type for all endpoint identities. |
| [_WS_ENDPOINT_POLICY_EXTENSION structure](..\webservices\ns-webservices-_ws_endpoint_policy_extension.md) | This structure is used to specify an endpoint policy extension. |
| [_WS_ENUM_DESCRIPTION structure](..\webservices\ns-webservices-_ws_enum_description.md) | A type description that is used with WS_ENUM_TYPE and is required. It provides information used in serializing and deserializing values of an enumeration. |
| [_WS_ENUM_VALUE structure](..\webservices\ns-webservices-_ws_enum_value.md) | Provides serialization information about a single value that is part of an enumeration (WS_ENUM_DESCRIPTION). |
| [_WS_ERROR_PROPERTY structure](..\webservices\ns-webservices-_ws_error_property.md) | Specifies an error specific setting. |
| [_WS_FAULT structure](..\webservices\ns-webservices-_ws_fault.md) | A Fault is a value carried in the body of a message which conveys a processing failure. Faults are modeled using the WS_FAULT structure. |
| [_WS_FAULT_CODE structure](..\webservices\ns-webservices-_ws_fault_code.md) | Represents a fault code. |
| [_WS_FAULT_DESCRIPTION structure](..\webservices\ns-webservices-_ws_fault_description.md) | Information about a mapping between an WS_FAULT and an XML element. |
| [_WS_FAULT_DETAIL_DESCRIPTION structure](..\webservices\ns-webservices-_ws_fault_detail_description.md) | A description of the detail element of a fault message. |
| [_WS_FAULT_REASON structure](..\webservices\ns-webservices-_ws_fault_reason.md) | Contains an explanation of the fault. |
| [_WS_FIELD_DESCRIPTION structure](..\webservices\ns-webservices-_ws_field_description.md) | Represents serialization information about a field within a structure. |
| [_WS_FLOAT_DESCRIPTION structure](..\webservices\ns-webservices-_ws_float_description.md) | An optional type description used with WS_FLOAT_TYPE to specify constraints on the set of values which can be deserialized. |
| [_WS_GUID_DESCRIPTION structure](..\webservices\ns-webservices-_ws_guid_description.md) | An optional type description used with WS_GUID_TYPE to specify constraints on the set of values which can be deserialized. |
| [_WS_HEAP_PROPERTIES structure](..\webservices\ns-webservices-_ws_heap_properties.md) | A structure that is used to specify a set of WS_HEAP_PROPERTYs. |
| [_WS_HEAP_PROPERTY structure](..\webservices\ns-webservices-_ws_heap_property.md) | Specifies a heap specific setting. |
| [_WS_HOST_NAMES structure](..\webservices\ns-webservices-_ws_host_names.md) | A structure containing a list of host names. |
| [_WS_HTTPS_URL structure](..\webservices\ns-webservices-_ws_https_url.md) | The URL subtype for specifying an HTTPS URL. |
| [_WS_HTTP_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_http_binding_template.md) | HTTP template structure to be filled in by application for http binding. |
| [_WS_HTTP_HEADER_AUTH_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_http_header_auth_binding_template.md) | HTTP header authentication security template information to be filled in by application. Associated with WS_HTTP_HEADER_AUTH_BINDING_TEMPLATE_TYPE. |
| [_WS_HTTP_HEADER_AUTH_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_http_header_auth_policy_description.md) | Describes the policy specifying http channel binding. |
| [_WS_HTTP_HEADER_AUTH_SECURITY_BINDING structure](..\webservices\ns-webservices-_ws_http_header_auth_security_binding.md) | The security binding subtype for specifying the use of HTTP header authentication against a target service or a HTTP proxy server based on the basic, digest (RFC 2617) and the SPNEGO (RFC4559) protocols. |
| [_WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT structure](..\webservices\ns-webservices-_ws_http_header_auth_security_binding_constraint.md) | A security binding constraint that corresponds to the WS_HTTP_HEADER_AUTH_SECURITY_BINDING. |
| [_WS_HTTP_HEADER_AUTH_SECURITY_BINDING_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_http_header_auth_security_binding_policy_description.md) | This type description is used with template APIs to describe the templates generated accordingly to input policy setting. |
| [_WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_http_header_auth_security_binding_template.md) | The security binding template for specifying the use of HTP header authentication protocol based security. |
| [_WS_HTTP_HEADER_MAPPING structure](..\webservices\ns-webservices-_ws_http_header_mapping.md) | Specifies an individual header that is mapped as part of WS_HTTP_MESSAGE_MAPPING. |
| [_WS_HTTP_MESSAGE_MAPPING structure](..\webservices\ns-webservices-_ws_http_message_mapping.md) | How an HTTP request or response should be represented in a message object. |
| [_WS_HTTP_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_http_policy_description.md) | Describes the policy specifying http channel binding. |
| [_WS_HTTP_REDIRECT_CALLBACK_CONTEXT structure](..\webservices\ns-webservices-_ws_http_redirect_callback_context.md) | Specifies the callback function and state for controlling the HTTP auto redirection behavior. |
| [_WS_HTTP_SSL_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_http_ssl_binding_template.md) | SSL security template information to be filled in by application. Associated with WS_HTTP_SSL_BINDING_TEMPLATE_TYPE. |
| [_WS_HTTP_SSL_HEADER_AUTH_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_http_ssl_header_auth_binding_template.md) | Username/password security template information to be filled in by application. Associated with WS_HTTP_SSL_HEADER_AUTH_BINDING_TEMPLATE_TYPE. |
| [_WS_HTTP_SSL_HEADER_AUTH_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_http_ssl_header_auth_policy_description.md) | Describes the policy specifying http channel binding with SSL transport security and header authentication. |
| [_WS_HTTP_SSL_KERBEROS_APREQ_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_http_ssl_kerberos_apreq_binding_template.md) | Username/password security template information to be filled in by application. Associated with WS_HTTP_SSL_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE. |
| [_WS_HTTP_SSL_KERBEROS_APREQ_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_http_ssl_kerberos_apreq_policy_description.md) | Describes the policy specifying http channel binding with SSL transport security and KERBEROS AP_REQ message security. |
| [_WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_http_ssl_kerberos_apreq_security_context_binding_template.md) | Security template information to be filled in by application. Associated with WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE. |
| [_WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_http_ssl_kerberos_apreq_security_context_policy_description.md) | Describes the policy specifying security context message binding over http channel binding, with SSL transport security. The bootstrap channel uses http channel binding with SSL transport security and KERBEROS AP_REQ message security. |
| [_WS_HTTP_SSL_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_http_ssl_policy_description.md) | Describes the policy specifying http channel binding. |
| [_WS_HTTP_SSL_USERNAME_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_http_ssl_username_binding_template.md) | Username/password security template information to be filled in by application. Associated with WS_HTTP_SSL_USERNAME_BINDING_TEMPLATE_TYPE. |
| [_WS_HTTP_SSL_USERNAME_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_http_ssl_username_policy_description.md) | Describes the policy specifying http channel binding with SSL transport security and username/password message security. |
| [_WS_HTTP_SSL_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_http_ssl_username_security_context_binding_template.md) | Security template information to be filled in by application. Associated with WS_HTTP_SSL_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE. |
| [_WS_HTTP_SSL_USERNAME_SECURITY_CONTEXT_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_http_ssl_username_security_context_policy_description.md) | Describes the policy specifying security context message binding over http channel binding, with SSL transport security. The bootstrap channel uses http channel binding with SSL transport security and username/password message security. |
| [_WS_HTTP_URL structure](..\webservices\ns-webservices-_ws_http_url.md) | The URL subtype for specifying an HTTP URL. |
| [_WS_INT16_DESCRIPTION structure](..\webservices\ns-webservices-_ws_int16_description.md) | An optional type description used with WS_INT16_TYPE to specify constraints on the set of values which can be deserialized. |
| [_WS_INT32_DESCRIPTION structure](..\webservices\ns-webservices-_ws_int32_description.md) | An optional type description used with WS_INT32_TYPE to specify constraints on the set of values which can be deserialized. |
| [_WS_INT64_DESCRIPTION structure](..\webservices\ns-webservices-_ws_int64_description.md) | An optional type description used with WS_INT64_TYPE to specify constraints on the set of values which can be deserialized. |
| [_WS_INT8_DESCRIPTION structure](..\webservices\ns-webservices-_ws_int8_description.md) | An optional type description used with WS_INT8_TYPE to specify constraints on the set of values which can be deserialized. |
| [_WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT structure](..\webservices\ns-webservices-_ws_issued_token_message_security_binding_constraint.md) | A security binding constraint that can be used to extract information about how to obtain an issued token from an issuing party. |
| [_WS_ITEM_RANGE structure](..\webservices\ns-webservices-_ws_item_range.md) | Defines the minimum and maximum number of items that may appear when using WS_REPEATING_ELEMENT_FIELD_MAPPING, WS_REPEATING_ELEMENT_CHOICE_FIELD_MAPPING, or WS_REPEATING_ANY_ELEMENT_FIELD_MAPPING within a WS_FIELD_DESCRIPTION. |
| [_WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING structure](..\webservices\ns-webservices-_ws_kerberos_apreq_message_security_binding.md) | The security binding subtype for specifying the use of the Kerberos AP_REQ ticket as a direct (i.e., without establishing a session) security token with WS-Security. |
| [_WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT structure](..\webservices\ns-webservices-_ws_kerberos_apreq_message_security_binding_constraint.md) | A security binding constraint that corresponds to the WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING. |
| [_WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_kerberos_apreq_message_security_binding_policy_description.md) | This type description is used with template APIs to describe the templates generated accordingly to input policy setting. |
| [_WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_kerberos_apreq_message_security_binding_template.md) | The security binding template for specifying the use of the Kerberos AP_REQ ticket as a direct (i.e., without establishing a session) security token with WS-Security. |
| [_WS_LISTENER_PROPERTIES structure](..\webservices\ns-webservices-_ws_listener_properties.md) | Specifies a set of WS_LISTENER_PROPERTY structures. |
| [_WS_LISTENER_PROPERTY structure](..\webservices\ns-webservices-_ws_listener_property.md) | Specifies a listener specific setting. |
| [_WS_MESSAGE_DESCRIPTION structure](..\webservices\ns-webservices-_ws_message_description.md) | The schema for the input/output WS_MESSAGE for a given operation description. |
| [_WS_MESSAGE_PROPERTIES structure](..\webservices\ns-webservices-_ws_message_properties.md) | Specifies a set of WS_MESSAGE_PROPERTY structures. |
| [_WS_MESSAGE_PROPERTY structure](..\webservices\ns-webservices-_ws_message_property.md) | Specifies a message specific setting. |
| [_WS_METADATA_ENDPOINT structure](..\webservices\ns-webservices-_ws_metadata_endpoint.md) | Information about a single endpoint that was read from metadata documents. |
| [_WS_METADATA_ENDPOINTS structure](..\webservices\ns-webservices-_ws_metadata_endpoints.md) | Information about all endpoints that were read from metadata documents. |
| [_WS_METADATA_PROPERTY structure](..\webservices\ns-webservices-_ws_metadata_property.md) | Specifies a metadata object setting. |
| [_WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING structure](..\webservices\ns-webservices-_ws_namedpipe_sspi_transport_security_binding.md) | The security binding subtype for specifying the use of the Windows Integrated Authentication protocol (such as Kerberos, NTLM or SPNEGO) with the named pipe transport. |
| [_WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE structure](..\webservices\ns-webservices-_ws_ncrypt_asymmetric_security_key_handle.md) | The type for specifying asymmetric cryptographic keys as a CryptoNG NCRYPT_KEY_HANDLE. |
| [_WS_NETPIPE_URL structure](..\webservices\ns-webservices-_ws_netpipe_url.md) | The URL subtype for specifying an net.pipe URL. |
| [_WS_NETTCP_URL structure](..\webservices\ns-webservices-_ws_nettcp_url.md) | The URL subtype for specifying an net.tcp URL. |
| [_WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure](..\webservices\ns-webservices-_ws_opaque_windows_integrated_auth_credential.md) | Type for supplying a Windows Integrated Authentication credential as an opaque handle created by SspiPromptForCredentials and the related family of APIs. This feature is available only on Windows 7 and later. |
| [_WS_OPERATION_DESCRIPTION structure](..\webservices\ns-webservices-_ws_operation_description.md) | Metadata for the service operation. |
| [_WS_PARAMETER_DESCRIPTION structure](..\webservices\ns-webservices-_ws_parameter_description.md) | The index of the parameters in the incoming/outgoing messages field descriptions. |
| [_WS_POLICY_CONSTRAINTS structure](..\webservices\ns-webservices-_ws_policy_constraints.md) | Specifies policy constraints for a channel. |
| [_WS_POLICY_EXTENSION structure](..\webservices\ns-webservices-_ws_policy_extension.md) | The base class for all policy extension structures. Policy extensions are assertions that are directly handled by applications such as custom assertions. |
| [_WS_POLICY_PROPERTIES structure](..\webservices\ns-webservices-_ws_policy_properties.md) | Specifies a set of WS_POLICY_PROPERTY structures. |
| [_WS_POLICY_PROPERTY structure](..\webservices\ns-webservices-_ws_policy_property.md) | Specifies a policy object setting. |
| [_WS_PROXY_MESSAGE_CALLBACK_CONTEXT structure](..\webservices\ns-webservices-_ws_proxy_message_callback_context.md) | Specifies the callback function and state for an application that wishes to associate or inspect headers in an input or an output message respectively. See also, WS_CALL_PROPERTY_SEND_MESSAGE_CONTEXT and WS_CALL_PROPERTY_RECEIVE_MESSAGE_CONTEXT. |
| [_WS_PROXY_PROPERTY structure](..\webservices\ns-webservices-_ws_proxy_property.md) | Specifies a proxy property. |
| [_WS_RAW_SYMMETRIC_SECURITY_KEY_HANDLE structure](..\webservices\ns-webservices-_ws_raw_symmetric_security_key_handle.md) | The type for specifying a symmetric cryptographic key as raw bytes. |
| [_WS_REQUEST_SECURITY_TOKEN_PROPERTY structure](..\webservices\ns-webservices-_ws_request_security_token_property.md) | Specifies a property for requesting a security token from an issuer. |
| [_WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT structure](..\webservices\ns-webservices-_ws_request_security_token_property_constraint.md) | This structure is used to specify a set of constraints for a particular request security token property. Any property constraints that are not specified will use the default constraints. |
| [_WS_RSA_ENDPOINT_IDENTITY structure](..\webservices\ns-webservices-_ws_rsa_endpoint_identity.md) | Type for RSA endpoint identity. |
| [_WS_SAML_AUTHENTICATOR structure](..\webservices\ns-webservices-_ws_saml_authenticator.md) | The abstract base type for all SAML authenticators used on the server side to validate incoming SAML tokens. |
| [_WS_SAML_MESSAGE_SECURITY_BINDING structure](..\webservices\ns-webservices-_ws_saml_message_security_binding.md) | The security binding subtype for specifying the use of a SAML assertion as a message security token. |
| [_WS_SECURITY_ALGORITHM_PROPERTY structure](..\webservices\ns-webservices-_ws_security_algorithm_property.md) | Specifies a cryptographic algorithm setting. |
| [_WS_SECURITY_ALGORITHM_SUITE structure](..\webservices\ns-webservices-_ws_security_algorithm_suite.md) | Defines the security algorithms and key lengths to be used with WS-Security. This setting is relevant to message security bindings and mixed-mode security bindings. |
| [_WS_SECURITY_BINDING structure](..\webservices\ns-webservices-_ws_security_binding.md) | The abstract base type for all security bindings. |
| [_WS_SECURITY_BINDING_CONSTRAINT structure](..\webservices\ns-webservices-_ws_security_binding_constraint.md) | The base class for all security binding constraint structures. |
| [_WS_SECURITY_BINDING_PROPERTIES structure](..\webservices\ns-webservices-_ws_security_binding_properties.md) | Specifies an array of security binding settings. |
| [_WS_SECURITY_BINDING_PROPERTY structure](..\webservices\ns-webservices-_ws_security_binding_property.md) | Specifies a security binding specific setting. |
| [_WS_SECURITY_BINDING_PROPERTY_CONSTRAINT structure](..\webservices\ns-webservices-_ws_security_binding_property_constraint.md) | This structure is used to specify a set of constraints for a particular security binding property. Any property constraints that are not specified will use the default constraints. |
| [_WS_SECURITY_CONSTRAINTS structure](..\webservices\ns-webservices-_ws_security_constraints.md) | This structure specifies the security related constraints as part of WS_POLICY_CONSTRAINTS. |
| [_WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING structure](..\webservices\ns-webservices-_ws_security_context_message_security_binding.md) | The security binding subtype for specifying the use of a security context token negotiated between the client and server using WS-SecureConversation. |
| [_WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT structure](..\webservices\ns-webservices-_ws_security_context_message_security_binding_constraint.md) | A security binding constraint that corresponds to the WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING. |
| [_WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_security_context_message_security_binding_policy_description.md) | This type description is used with template APIs to describe the templates generated accordingly to input policy setting. |
| [_WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_security_context_message_security_binding_template.md) | The security binding template for specifying the use of an application supplied security context security binding. |
| [_WS_SECURITY_CONTEXT_PROPERTY structure](..\webservices\ns-webservices-_ws_security_context_property.md) | Defines a property of a WS_SECURITY_CONTEXT |
| [_WS_SECURITY_CONTEXT_SECURITY_BINDING_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_security_context_security_binding_policy_description.md) | This type description is used with template APIs to describe the security context related templates generated accordingly to input policy setting. |
| [_WS_SECURITY_CONTEXT_SECURITY_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_security_context_security_binding_template.md) | The security binding template for specifying the use of an application supplied security context security binding. |
| [_WS_SECURITY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_security_description.md) | The top-level structure used to specify the security requirements for a channel (on the client side) or a listener (on the server side). |
| [_WS_SECURITY_KEY_HANDLE structure](..\webservices\ns-webservices-_ws_security_key_handle.md) | The abstract base type for all types that specify a cryptographic key. Such a key is typically specified for a generic XML security token or a custom security token. |
| [_WS_SECURITY_PROPERTIES structure](..\webservices\ns-webservices-_ws_security_properties.md) | Specifies an array of channel-wide security settings. |
| [_WS_SECURITY_PROPERTY structure](..\webservices\ns-webservices-_ws_security_property.md) | Specifies a channel-wide security setting. |
| [_WS_SECURITY_PROPERTY_CONSTRAINT structure](..\webservices\ns-webservices-_ws_security_property_constraint.md) | This structure is used to specify a set of constraints for a particular security property. Any property constraints that are not specified will use the default constraints. |
| [_WS_SERVICE_CONTRACT structure](..\webservices\ns-webservices-_ws_service_contract.md) | Specifies a service contract on an endpoint. |
| [_WS_SERVICE_ENDPOINT structure](..\webservices\ns-webservices-_ws_service_endpoint.md) | Represents an individual endpoint on a service host. The properties on the endpoint are used to specify the address, binding and contract. |
| [_WS_SERVICE_ENDPOINT_METADATA structure](..\webservices\ns-webservices-_ws_service_endpoint_metadata.md) | Represents the port element for the endpoint. The port element is generated for the service element as specified by serviceName and serviceNs for WS_SERVICE_PROPERTY_METADATA property on the WS_SERVICE_HOST. |
| [_WS_SERVICE_ENDPOINT_PROPERTY structure](..\webservices\ns-webservices-_ws_service_endpoint_property.md) | Specifies a service specific setting. |
| [_WS_SERVICE_METADATA structure](..\webservices\ns-webservices-_ws_service_metadata.md) | Specifies the service metadata documents array. This can be a collection of WSDL/XSD documents represented as an array of WS_STRING. |
| [_WS_SERVICE_METADATA_DOCUMENT structure](..\webservices\ns-webservices-_ws_service_metadata_document.md) | Specifies the individual documents that make up the service metadata. |
| [_WS_SERVICE_PROPERTY structure](..\webservices\ns-webservices-_ws_service_property.md) | Specifies a service specific setting. |
| [_WS_SERVICE_PROPERTY_ACCEPT_CALLBACK structure](..\webservices\ns-webservices-_ws_service_property_accept_callback.md) | Specifies the callback which is called when a channel is successfully accepted. |
| [_WS_SERVICE_PROPERTY_CLOSE_CALLBACK structure](..\webservices\ns-webservices-_ws_service_property_close_callback.md) | Specifies the callback which is called when a channel is about to be closed. See, WS_SERVICE_CLOSE_CHANNEL_CALLBACK for details. |
| [_WS_SERVICE_SECURITY_IDENTITIES structure](..\webservices\ns-webservices-_ws_service_security_identities.md) | A list of Server Principal Names (SPNs) that are used to validate Extended Protection. |
| [_WS_SOAPUDP_URL structure](..\webservices\ns-webservices-_ws_soapudp_url.md) | The URL subtype for specifying an soap.udp URL. |
| [_WS_SPN_ENDPOINT_IDENTITY structure](..\webservices\ns-webservices-_ws_spn_endpoint_identity.md) | Type for specifying an endpoint identity represented by an SPN (service principal name). |
| [_WS_SSL_TRANSPORT_SECURITY_BINDING structure](..\webservices\ns-webservices-_ws_ssl_transport_security_binding.md) | The security binding subtype for specifying the use of SSL/TLS protocol based transport security. |
| [_WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT structure](..\webservices\ns-webservices-_ws_ssl_transport_security_binding_constraint.md) | A security binding constraint that corresponds to the WS_SSL_TRANSPORT_SECURITY_BINDING. |
| [_WS_SSL_TRANSPORT_SECURITY_BINDING_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_ssl_transport_security_binding_policy_description.md) | This type description is used with template APIs to describe the templates generated accordingly to input policy setting. |
| [_WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_ssl_transport_security_binding_template.md) | The security binding template for specifying the use of SSL/TLS protocol based transport security. See also WS_SSL_TRANSPORT_SECURITY_BINDING .This security binding is supported only with the WS_HTTP_CHANNEL_BINDING. |
| [_WS_SSPI_TRANSPORT_SECURITY_BINDING_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_sspi_transport_security_binding_policy_description.md) | This type description is used with template APIs to describe the templates generated accordingly to input policy setting. |
| [_WS_STRING structure](..\webservices\ns-webservices-_ws_string.md) | An array of Unicode characters and a length. |
| [_WS_STRING_DESCRIPTION structure](..\webservices\ns-webservices-_ws_string_description.md) | This type description is used with WS_STRING_TYPE and is optional. It is used to specify constraints on the set of values which can be deserialized. |
| [_WS_STRING_USERNAME_CREDENTIAL structure](..\webservices\ns-webservices-_ws_string_username_credential.md) | The type for supplying a username/password pair as strings. |
| [_WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure](..\webservices\ns-webservices-_ws_string_windows_integrated_auth_credential.md) | Type for supplying a Windows credential as username, password, domain strings. |
| [_WS_STRUCT_DESCRIPTION structure](..\webservices\ns-webservices-_ws_struct_description.md) | Information about C struct type, and how it maps to an XML element. This is used with WS_STRUCT_TYPE. |
| [_WS_SUBJECT_NAME_CERT_CREDENTIAL structure](..\webservices\ns-webservices-_ws_subject_name_cert_credential.md) | The type for specifying a certificate credential using the certificate's subject name, store location and store name. The specified credential is loaded when the containing channel or listener is opened. |
| [_WS_TCP_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_tcp_binding_template.md) | TCP template structure to be filled in by application for TCP binding. |
| [_WS_TCP_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_tcp_policy_description.md) | Describes the policy specifying http channel binding. |
| [_WS_TCP_SSPI_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_tcp_sspi_binding_template.md) | HTTP header authentication security template information to be filled in by application. Associated with WS_TCP_SSPI_BINDING_TEMPLATE_TYPE. |
| [_WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_tcp_sspi_kerberos_apreq_binding_template.md) | Username/password security template information to be filled in by application. Associated with WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE. |
| [_WS_TCP_SSPI_KERBEROS_APREQ_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_tcp_sspi_kerberos_apreq_policy_description.md) | Describes the policy specifying TCP channel binding with windows SSPI transport security, and kerberos message security. |
| [_WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_tcp_sspi_kerberos_apreq_security_context_binding_template.md) | Security template information to be filled in by application. Associated with WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE. |
| [_WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_tcp_sspi_kerberos_apreq_security_context_policy_description.md) | Describes the policy specifying security context message binding using TCP channel binding with windows SSPI transport security. The bootstrap channel uses TCP channel binding with windows SSPI transport security and kerberos message security. |
| [_WS_TCP_SSPI_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_tcp_sspi_policy_description.md) | Describes the policy specifying TCP channel binding with windows SSPI. |
| [_WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING structure](..\webservices\ns-webservices-_ws_tcp_sspi_transport_security_binding.md) | The security binding subtype for specifying the use of the Windows Integrated Authentication protocol (such as Kerberos, NTLM or SPNEGO) with the TCP transport. |
| [_WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT structure](..\webservices\ns-webservices-_ws_tcp_sspi_transport_security_binding_constraint.md) | A security binding constraint that corresponds to the WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING. |
| [_WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_tcp_sspi_transport_security_binding_template.md) | The security binding template for specifying the use of Windows SSPI protocol based transport security. See also WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING. |
| [_WS_TCP_SSPI_USERNAME_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_tcp_sspi_username_binding_template.md) | Username/password security template information to be filled in by application. Associated with WS_TCP_SSPI_USERNAME_BINDING_TEMPLATE_TYPE. |
| [_WS_TCP_SSPI_USERNAME_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_tcp_sspi_username_policy_description.md) | Describes the policy specifying TCP channel binding with windows SSPI transport security and username/password message security. |
| [_WS_TCP_SSPI_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_tcp_sspi_username_security_context_binding_template.md) | Security template information to be filled in by application. Associated with WS_TCP_SSPI_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE. |
| [_WS_TCP_SSPI_USERNAME_SECURITY_CONTEXT_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_tcp_sspi_username_security_context_policy_description.md) | Describes the policy specifying security context message binding using TCP channel binding with windows SSPI transport security. The bootstrap channel uses TCP channel binding with windows SSPI transport security and username/password message security. |
| [_WS_THUMBPRINT_CERT_CREDENTIAL structure](..\webservices\ns-webservices-_ws_thumbprint_cert_credential.md) | The type for specifying a certificate credential using the certificate's thumbprint, store location and store name. |
| [_WS_TIMESPAN structure](..\webservices\ns-webservices-_ws_timespan.md) | Represents a signed 64-bit time interval in 100 nanosecond units. |
| [_WS_TIMESPAN_DESCRIPTION structure](..\webservices\ns-webservices-_ws_timespan_description.md) | This type description is used with WS_TIMESPAN_TYPE and is optional. It is used to specify constraints on the set of values which can be deserialized. |
| [_WS_UINT16_DESCRIPTION structure](..\webservices\ns-webservices-_ws_uint16_description.md) | An optional type description used with WS_UINT16_TYPE to specify constraints on the set of values which can be deserialized. |
| [_WS_UINT32_DESCRIPTION structure](..\webservices\ns-webservices-_ws_uint32_description.md) | An optional type description used with WS_UINT32_TYPE to specify constraints on the set of values which can be deserialized. |
| [_WS_UINT64_DESCRIPTION structure](..\webservices\ns-webservices-_ws_uint64_description.md) | An optional type description used with WS_UINT64_TYPE to specify constraints on the set of values which can be deserialized. |
| [_WS_UINT8_DESCRIPTION structure](..\webservices\ns-webservices-_ws_uint8_description.md) | An optional type description used with WS_UINT8_TYPE to specify constraints on the set of values which can be deserialized. |
| [_WS_UNION_DESCRIPTION structure](..\webservices\ns-webservices-_ws_union_description.md) | Information about the choices within a union type. This is used with WS_UNION_TYPE. |
| [_WS_UNION_FIELD_DESCRIPTION structure](..\webservices\ns-webservices-_ws_union_field_description.md) | Represents serialization information about a field within a union. See WS_UNION_DESCRIPTION. |
| [_WS_UNIQUE_ID structure](..\webservices\ns-webservices-_ws_unique_id.md) | Represents a unique ID URI. |
| [_WS_UNIQUE_ID_DESCRIPTION structure](..\webservices\ns-webservices-_ws_unique_id_description.md) | An optional type description used with WS_UNIQUE_ID_TYPE to specify constraints on the set of values which can be deserialized. |
| [_WS_UNKNOWN_ENDPOINT_IDENTITY structure](..\webservices\ns-webservices-_ws_unknown_endpoint_identity.md) | Type for unknown endpoint identity. This type is only used to represent an endpoint identity type that was deserialized but was not understood. |
| [_WS_UPN_ENDPOINT_IDENTITY structure](..\webservices\ns-webservices-_ws_upn_endpoint_identity.md) | Type for specifying an endpoint identity represented by a UPN (user principal name). |
| [_WS_URL structure](..\webservices\ns-webservices-_ws_url.md) | The abstract base type for all URL schemes used with WsDecodeUrl and WsEncodeUrl APIs. |
| [_WS_USERNAME_CREDENTIAL structure](..\webservices\ns-webservices-_ws_username_credential.md) | The abstract base type for all username/password credentials. |
| [_WS_USERNAME_MESSAGE_SECURITY_BINDING structure](..\webservices\ns-webservices-_ws_username_message_security_binding.md) | The security binding subtype for specifying the use of an application supplied username / password pair as a direct (i.e., one-shot) security token. |
| [_WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT structure](..\webservices\ns-webservices-_ws_username_message_security_binding_constraint.md) | A security binding constraint that corresponds to the WS_USERNAME_MESSAGE_SECURITY_BINDING. |
| [_WS_USERNAME_MESSAGE_SECURITY_BINDING_POLICY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_username_message_security_binding_policy_description.md) | This type description is used with template APIs to describe the templates generated accordingly to input policy setting. |
| [_WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE structure](..\webservices\ns-webservices-_ws_username_message_security_binding_template.md) | The security binding template for specifying the use of an application supplied username / password pair as a direct (i.e., one-shot) security token. |
| [_WS_UTF8_ARRAY_DESCRIPTION structure](..\webservices\ns-webservices-_ws_utf8_array_description.md) | This type description is used with WS_UTF8_ARRAY_TYPE and is optional. It is used to specify constraints on the set of values which can be deserialized. |
| [_WS_VOID_DESCRIPTION structure](..\webservices\ns-webservices-_ws_void_description.md) | Specifies information about a field which is neither serialized nor deserialized. This is used with WS_VOID_TYPE and WS_NO_FIELD_MAPPING within a WS_FIELD_DESCRIPTION. This type description is only required when WS_FIELD_POINTER is not being used. |
| [_WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure](..\webservices\ns-webservices-_ws_windows_integrated_auth_credential.md) | The abstract base type for all credential types used with Windows Integrated Authentication. |
| [_WS_WSZ_DESCRIPTION structure](..\webservices\ns-webservices-_ws_wsz_description.md) | This type description is used with WS_WSZ_TYPE and is optional. It is used to specify constraints on the set of values which can be deserialized. |
| [_WS_XML_ATTRIBUTE structure](..\webservices\ns-webservices-_ws_xml_attribute.md) | Represents an attribute (for example, &lt;a |
| [_WS_XML_BASE64_TEXT structure](..\webservices\ns-webservices-_ws_xml_base64_text.md) | Represents base64 encoded data. |
| [_WS_XML_BOOL_TEXT structure](..\webservices\ns-webservices-_ws_xml_bool_text.md) | A Boolean value that represents the text &#0034;true&#0034; or &#0034;false&#0034;. |
| [_WS_XML_BUFFER_PROPERTY structure](..\webservices\ns-webservices-_ws_xml_buffer_property.md) | Specifies an XML buffer&#8211;specific setting. |
| [_WS_XML_CANONICALIZATION_INCLUSIVE_PREFIXES structure](..\webservices\ns-webservices-_ws_xml_canonicalization_inclusive_prefixes.md) | An array of XML prefixes that should be treated as inclusive prefixes during exclusive XML canonicalization. The treatment of inclusive prefixes is defined in RFC 3741. |
| [_WS_XML_CANONICALIZATION_PROPERTY structure](..\webservices\ns-webservices-_ws_xml_canonicalization_property.md) | Specifies a setting that controls how XML canonicalization is done. |
| [_WS_XML_COMMENT_NODE structure](..\webservices\ns-webservices-_ws_xml_comment_node.md) | Represents a comment. |
| [_WS_XML_DATETIME_TEXT structure](..\webservices\ns-webservices-_ws_xml_datetime_text.md) | Represents a datetime formatted as an xsd |
| [_WS_XML_DECIMAL_TEXT structure](..\webservices\ns-webservices-_ws_xml_decimal_text.md) | Represents a 12 byte fixed point value. |
| [_WS_XML_DICTIONARY structure](..\webservices\ns-webservices-_ws_xml_dictionary.md) | Represents a set of unique strings. This information is used by the binary encoding to write a more compact xml document. |
| [_WS_XML_DOUBLE_TEXT structure](..\webservices\ns-webservices-_ws_xml_double_text.md) | Represents an 8 byte floating point value. |
| [_WS_XML_ELEMENT_NODE structure](..\webservices\ns-webservices-_ws_xml_element_node.md) | Represents a start element in xml (e.g. |
| [_WS_XML_FLOAT_TEXT structure](..\webservices\ns-webservices-_ws_xml_float_text.md) | Represents a 4 byte floating point value. |
| [_WS_XML_GUID_TEXT structure](..\webservices\ns-webservices-_ws_xml_guid_text.md) | Represents a GUID formatted as the text &#0034;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx&#0034;. |
| [_WS_XML_INT32_TEXT structure](..\webservices\ns-webservices-_ws_xml_int32_text.md) | Represents a signed 32 bit integer. |
| [_WS_XML_INT64_TEXT structure](..\webservices\ns-webservices-_ws_xml_int64_text.md) | Represents a signed 64 bit integer. |
| [_WS_XML_LIST_TEXT structure](..\webservices\ns-webservices-_ws_xml_list_text.md) | Represents a list of text values separated by a single whitespace character. |
| [_WS_XML_NODE structure](..\webservices\ns-webservices-_ws_xml_node.md) | The base type for all the different kinds of XML nodes. An XML node is unit of data in XML. |
| [_WS_XML_NODE_POSITION structure](..\webservices\ns-webservices-_ws_xml_node_position.md) | Represents a position within an XML buffer. |
| [_WS_XML_QNAME structure](..\webservices\ns-webservices-_ws_xml_qname.md) | A structure used to specify an XML name (of an element or an attribute) as a local name, namespace pair. |
| [_WS_XML_QNAME_DESCRIPTION structure](..\webservices\ns-webservices-_ws_xml_qname_description.md) | This type description is used with WS_XML_QNAME_TYPE and is optional. It is used to specify constraints on the set of values which can be deserialized. |
| [_WS_XML_QNAME_TEXT structure](..\webservices\ns-webservices-_ws_xml_qname_text.md) | Represents a qname formatted as the text &#0034;prefix |
| [_WS_XML_READER_BINARY_ENCODING structure](..\webservices\ns-webservices-_ws_xml_reader_binary_encoding.md) | Used to indicate that the reader should interpret the bytes it reads as binary xml. |
| [_WS_XML_READER_BUFFER_INPUT structure](..\webservices\ns-webservices-_ws_xml_reader_buffer_input.md) | Specifies that the source of the xml input is a buffer. |
| [_WS_XML_READER_ENCODING structure](..\webservices\ns-webservices-_ws_xml_reader_encoding.md) | This structure is the base type for all the different kinds of reader encodings. |
| [_WS_XML_READER_INPUT structure](..\webservices\ns-webservices-_ws_xml_reader_input.md) | Specifies where the reader should obtain the bytes that comprise the xml document. |
| [_WS_XML_READER_MTOM_ENCODING structure](..\webservices\ns-webservices-_ws_xml_reader_mtom_encoding.md) | Used to indicate that the reader should interpret the bytes it reads as in MTOM format. |
| [_WS_XML_READER_PROPERTIES structure](..\webservices\ns-webservices-_ws_xml_reader_properties.md) | A structure that is used to specify a set of WS_XML_READER_PROPERTYs. |
| [_WS_XML_READER_PROPERTY structure](..\webservices\ns-webservices-_ws_xml_reader_property.md) | Specifies a reader specific setting. |
| [_WS_XML_READER_RAW_ENCODING structure](..\webservices\ns-webservices-_ws_xml_reader_raw_encoding.md) | Used to indicate that the reader should surface the bytes of the document as base64 encoded characters. |
| [_WS_XML_READER_STREAM_INPUT structure](..\webservices\ns-webservices-_ws_xml_reader_stream_input.md) | Specifies that the source of the xml should be obtained from a callback. |
| [_WS_XML_READER_TEXT_ENCODING structure](..\webservices\ns-webservices-_ws_xml_reader_text_encoding.md) | Used to indicate that the reader should interpret the bytes it reads as textual xml. |
| [_WS_XML_SECURITY_TOKEN_PROPERTY structure](..\webservices\ns-webservices-_ws_xml_security_token_property.md) | Specifies a property for an XML security token. |
| [_WS_XML_STRING structure](..\webservices\ns-webservices-_ws_xml_string.md) | Represents a string that optionally has dictionary information associated with it. The xml APIs use WS_XML_STRINGs to identify prefixes, localNames and namespaces. |
| [_WS_XML_STRING_DESCRIPTION structure](..\webservices\ns-webservices-_ws_xml_string_description.md) | This type description is used with WS_XML_STRING_TYPE and is optional. It is used to specify constraints on the set of values which can be deserialized. |
| [_WS_XML_TEXT structure](..\webservices\ns-webservices-_ws_xml_text.md) | Represents a node of text content in xml. |
| [_WS_XML_TEXT_NODE structure](..\webservices\ns-webservices-_ws_xml_text_node.md) | Represents an element, attribute, or CDATA content. |
| [_WS_XML_TIMESPAN_TEXT structure](..\webservices\ns-webservices-_ws_xml_timespan_text.md) | Represents a time span formatted as the text &#0034;[+|-][d?.]HH |
| [_WS_XML_TOKEN_MESSAGE_SECURITY_BINDING structure](..\webservices\ns-webservices-_ws_xml_token_message_security_binding.md) | The security binding subtype for specifying the use of a security token that is already available to the application in XML form. |
| [_WS_XML_UINT64_TEXT structure](..\webservices\ns-webservices-_ws_xml_uint64_text.md) | Represents an unsigned 64 bit integer. |
| [_WS_XML_UNIQUE_ID_TEXT structure](..\webservices\ns-webservices-_ws_xml_unique_id_text.md) | Represents a GUID formatted as the text &#0034;urn |
| [_WS_XML_UTF16_TEXT structure](..\webservices\ns-webservices-_ws_xml_utf16_text.md) | Represents text encoded as UTF-16 bytes. |
| [_WS_XML_UTF8_TEXT structure](..\webservices\ns-webservices-_ws_xml_utf8_text.md) | Represents text encoded as UTF-8 bytes. |
| [_WS_XML_WRITER_BINARY_ENCODING structure](..\webservices\ns-webservices-_ws_xml_writer_binary_encoding.md) | Used to indicate that the writer should emit bytes as binary xml. |
| [_WS_XML_WRITER_BUFFER_OUTPUT structure](..\webservices\ns-webservices-_ws_xml_writer_buffer_output.md) | Specifies that the generated bytes should be placed in a buffer. |
| [_WS_XML_WRITER_ENCODING structure](..\webservices\ns-webservices-_ws_xml_writer_encoding.md) | This structure is the base type for all the different kinds of writer encodings. |
| [_WS_XML_WRITER_MTOM_ENCODING structure](..\webservices\ns-webservices-_ws_xml_writer_mtom_encoding.md) | Used to indicate that the reader should emit bytes in MTOM format. The MTOM format will represent bytes written to it as binary mime parts rather than embedded base64 encoded text. |
| [_WS_XML_WRITER_OUTPUT structure](..\webservices\ns-webservices-_ws_xml_writer_output.md) | Specifies where the writer should emit the bytes that comprise the xml document. |
| [_WS_XML_WRITER_PROPERTIES structure](..\webservices\ns-webservices-_ws_xml_writer_properties.md) | A structure that is used to specify a set of WS_XML_WRITER_PROPERTYs. |
| [_WS_XML_WRITER_PROPERTY structure](..\webservices\ns-webservices-_ws_xml_writer_property.md) | Specifies a writer specific setting. |
| [_WS_XML_WRITER_RAW_ENCODING structure](..\webservices\ns-webservices-_ws_xml_writer_raw_encoding.md) | Used to indicate that the writer should emit bytes from decoded base64 characters. |
| [_WS_XML_WRITER_STREAM_OUTPUT structure](..\webservices\ns-webservices-_ws_xml_writer_stream_output.md) | Specifies that the generated bytes should be sent to callback. |
| [_WS_XML_WRITER_TEXT_ENCODING structure](..\webservices\ns-webservices-_ws_xml_writer_text_encoding.md) | Indicates that the reader should emit bytes as textual xml. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [WS_ADDRESSING_VERSION enumeration](..\webservices\ne-webservices-ws_addressing_version.md) | Identifies the version of the specification used for the addressing headers. |
| [WS_BINDING_TEMPLATE_TYPE enumeration](..\webservices\ne-webservices-ws_binding_template_type.md) | An enumeration of the different security binding combinations that are supported. |
| [WS_CALLBACK_MODEL enumeration](..\webservices\ne-webservices-ws_callback_model.md) | Specifies the threading behavior of a callback (for example, a WS_ASYNC_CALLBACK). |
| [WS_CALL_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_call_property_id.md) | Optional parameters for configuring a call on a client side service operation. |
| [WS_CERT_CREDENTIAL_TYPE enumeration](..\webservices\ne-webservices-ws_cert_credential_type.md) | The type of the certificate credential, used as a selector for subtypes of WS_CERT_CREDENTIAL. |
| [WS_CHANNEL_BINDING enumeration](..\webservices\ne-webservices-ws_channel_binding.md) | Indicates the protocol stack to use for the channel. |
| [WS_CHANNEL_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_channel_property_id.md) | Each channel property is identified by an ID and has an associated value. If a property is not specified when the channel is created, then its default value is used. |
| [WS_CHANNEL_STATE enumeration](..\webservices\ne-webservices-ws_channel_state.md) | The different states that a channel can be in. |
| [WS_CHANNEL_TYPE enumeration](..\webservices\ne-webservices-ws_channel_type.md) | Indicates the basic characteristics of the channel, such as whether it is sessionful, and what directions of communication are supported. |
| [WS_CHARSET enumeration](..\webservices\ne-webservices-ws_charset.md) | Identifies the character set of a document. |
| [WS_COOKIE_MODE enumeration](..\webservices\ne-webservices-ws_cookie_mode.md) | An enumeration used to specify how to handle HTTP cookies. |
| [WS_DATETIME_FORMAT enumeration](..\webservices\ne-webservices-ws_datetime_format.md) | Specifies the textual format of a WS_DATETIME. |
| [WS_ENCODING enumeration](..\webservices\ne-webservices-ws_encoding.md) | The different encodings (message formats). |
| [WS_ENDPOINT_ADDRESS_EXTENSION_TYPE enumeration](..\webservices\ne-webservices-ws_endpoint_address_extension_type.md) | This identifies a type of extension within the extensions field of the WS_ENDPOINT_ADDRESS. |
| [WS_ENDPOINT_IDENTITY_TYPE enumeration](..\webservices\ne-webservices-ws_endpoint_identity_type.md) | The type of the endpoint IDentity, used as a selector for subtypes of WS_ENDPOINT_IDENTITY. |
| [WS_ENVELOPE_VERSION enumeration](..\webservices\ne-webservices-ws_envelope_version.md) | The version of the specification used for the envelope structure. |
| [WS_ERROR_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_error_property_id.md) | A set of property values associated with the error. They are set and retrieved using WsGetErrorProperty and WsSetErrorProperty. |
| [WS_EXCEPTION_CODE enumeration](..\webservices\ne-webservices-ws_exception_code.md) | The structured exception codes thrown by this component. These exceptions are fatal and should not be handled by the application. |
| [WS_EXTENDED_PROTECTION_POLICY enumeration](..\webservices\ne-webservices-ws_extended_protection_policy.md) | Defines if Extended Protection data should be validated. |
| [WS_EXTENDED_PROTECTION_SCENARIO enumeration](..\webservices\ne-webservices-ws_extended_protection_scenario.md) | Defines how Extended Protection is validated. |
| [WS_FAULT_DISCLOSURE enumeration](..\webservices\ne-webservices-ws_fault_disclosure.md) | Controls how much error information is included in a fault. Since the error object may contain sensitive data as part of the error string, it is not always appropriate to include the error strings information in all faults. |
| [WS_FAULT_ERROR_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_fault_error_property_id.md) | Information about a fault. |
| [WS_FIELD_MAPPING enumeration](..\webservices\ne-webservices-ws_field_mapping.md) | Specifies how a field of a structure is represented in XML. This is used within a WS_FIELD_DESCRIPTION. |
| [WS_HEADER_TYPE enumeration](..\webservices\ne-webservices-ws_header_type.md) | Identifies a type of header. |
| [WS_HEAP_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_heap_property_id.md) | Each heap property is identified by an ID and has an associated value. |
| [WS_HTTP_HEADER_AUTH_TARGET enumeration](..\webservices\ne-webservices-ws_http_header_auth_target.md) | Defines the target for the HTTP header authentication security binding. |
| [WS_HTTP_PROXY_SETTING_MODE enumeration](..\webservices\ne-webservices-ws_http_proxy_setting_mode.md) | Proxy setting indicates HTTP proxy setting for the channel with binding WS_HTTP_CHANNEL_BINDING. This is specified as part of WS_CHANNEL_PROPERTY_HTTP_PROXY_SETTING_MODE channel property. |
| [WS_IP_VERSION enumeration](..\webservices\ne-webservices-ws_ip_version.md) | Specifies an IP version. |
| [WS_LISTENER_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_listener_property_id.md) | Each listener property is of type WS_LISTENER_PROPERTY, is identified by an ID, and has an associated value. If a property is not specified when the listener is created, then its default value is used. |
| [WS_LISTENER_STATE enumeration](..\webservices\ne-webservices-ws_listener_state.md) | The different states that a listener can be in. |
| [WS_MESSAGE_INITIALIZATION enumeration](..\webservices\ne-webservices-ws_message_initialization.md) | Specifies what headers the WsInitializeMessage should add to the message. |
| [WS_MESSAGE_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_message_property_id.md) | Each message property is of type WS_MESSAGE_PROPERTY, is identified by an ID, and has an associated value. |
| [WS_MESSAGE_SECURITY_USAGE enumeration](..\webservices\ne-webservices-ws_message_security_usage.md) | Defines how a message security binding attaches the security token corresponding to it to a message using WS-Security mechanisms. |
| [WS_MESSAGE_STATE enumeration](..\webservices\ne-webservices-ws_message_state.md) | The different states that a message can be in. |
| [WS_METADATA_EXCHANGE_TYPE enumeration](..\webservices\ne-webservices-ws_metadata_exchange_type.md) | TBD |
| [WS_METADATA_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_metadata_property_id.md) | Each metadata property is of type WS_METADATA_PROPERTY, is identified by an ID, and has an associated value. If a property is not specified when the metadata is created, then its default value is used. |
| [WS_METADATA_STATE enumeration](..\webservices\ne-webservices-ws_metadata_state.md) | The state of the metadata object. |
| [WS_MOVE_TO enumeration](..\webservices\ne-webservices-ws_move_to.md) | This enumeration identifies the various ways to move about an xml document. |
| [WS_OPERATION_CONTEXT_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_operation_context_property_id.md) | The properties available on the Context. Not all properties may be available at a given point on a context. All context properties are available through WsGetOperationContextProperty. |
| [WS_OPERATION_STYLE enumeration](..\webservices\ne-webservices-ws_operation_style.md) | An enumeration of the different operation styles. |
| [WS_PARAMETER_TYPE enumeration](..\webservices\ne-webservices-ws_parameter_type.md) | The different parameter types. |
| [WS_POLICY_EXTENSION_TYPE enumeration](..\webservices\ne-webservices-ws_policy_extension_type.md) | The values in this enumeration are used to identify the sub-types of WS_POLICY_EXTENSION. |
| [WS_POLICY_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_policy_property_id.md) | Identifies each policy property and its associated value. |
| [WS_POLICY_STATE enumeration](..\webservices\ne-webservices-ws_policy_state.md) | The state of the policy object. |
| [WS_PROTECTION_LEVEL enumeration](..\webservices\ne-webservices-ws_protection_level.md) | Defines the required integrity and confidentiality levels for sent and received messages. |
| [WS_PROXY_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_proxy_property_id.md) | Optional parameters for configuring the service proxy. With an exception of WS_PROXY_PROPERTY_STATE all the values are only supported for use with WsCreateServiceProxy as part of the WS_PROXY_PROPERTY* parameter. |
| [WS_READ_OPTION enumeration](..\webservices\ne-webservices-ws_read_option.md) | Specifies whether a value is required, and how the value should be allocated. |
| [WS_RECEIVE_OPTION enumeration](..\webservices\ne-webservices-ws_receive_option.md) | Specifies whether a message is required when receiving from a channel. |
| [WS_REPEATING_HEADER_OPTION enumeration](..\webservices\ne-webservices-ws_repeating_header_option.md) | This enum is used to specify whether a header is expected to appear more than once in a message. |
| [WS_REQUEST_SECURITY_TOKEN_ACTION enumeration](..\webservices\ne-webservices-ws_request_security_token_action.md) | Defines which set of actions to use when negotiating security tokens using WS-Trust. |
| [WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_request_security_token_property_id.md) | Identifies the properties for requesting a security token from an issuer. It is used with WsRequestSecurityToken as part of the WS_REQUEST_SECURITY_TOKEN_PROPERTY* parameter. |
| [WS_SAML_AUTHENTICATOR_TYPE enumeration](..\webservices\ne-webservices-ws_saml_authenticator_type.md) | The type IDs of the SAML token authenticators used on the server side (For example, relying party) to validate incoming SAML tokens. |
| [WS_SECURE_CONVERSATION_VERSION enumeration](..\webservices\ne-webservices-ws_secure_conversation_version.md) | Defines the WS-SecureConversation specification version to be used with message security and mixed-mode security. |
| [WS_SECURITY_ALGORITHM_ID enumeration](..\webservices\ne-webservices-ws_security_algorithm_id.md) | Defines the security algorithms to be used with WS-Security. These values are relevant to message security bindings and mixed-mode security bindings. |
| [WS_SECURITY_ALGORITHM_PROPERTY_ID enumeration](..\webservices\ne-webservices-__unnamed_enum_7.md) | Identifies the properties representing security algorithm knobs. |
| [WS_SECURITY_ALGORITHM_SUITE_NAME enumeration](..\webservices\ne-webservices-ws_security_algorithm_suite_name.md) | A suite of security algorithms used for tasks such as signing and encryting. The values in this enumeration correspond to the suites defined in WS-SecurityPolicy 1.1 section 7.1. |
| [WS_SECURITY_BINDING_CONSTRAINT_TYPE enumeration](..\webservices\ne-webservices-ws_security_binding_constraint_type.md) | The values in this enumeration are used to identify the sub-types of WS_SECURITY_BINDING_CONSTRAINT. |
| [WS_SECURITY_BINDING_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_security_binding_property_id.md) | Identifies the properties used to specify security binding settings. Security binding settings are present in security bindings that are used, in turn, in a security description. |
| [WS_SECURITY_BINDING_TYPE enumeration](..\webservices\ne-webservices-ws_security_binding_type.md) | The type of the security binding, used as a selector for subtypes of WS_SECURITY_BINDING. |
| [WS_SECURITY_CONTEXT_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_security_context_property_id.md) | Identifies a property of a security context object. This enumeration is used with WsGetSecurityContextProperty. |
| [WS_SECURITY_HEADER_LAYOUT enumeration](..\webservices\ne-webservices-ws_security_header_layout.md) | The layout rules applied to the elements of the WS-Security security header. This setting is relevant to message security bindings and mixed-mode security bindings. |
| [WS_SECURITY_HEADER_VERSION enumeration](..\webservices\ne-webservices-ws_security_header_version.md) | The WS-Security specification version to be used with message security and mixed-mode security. |
| [WS_SECURITY_KEY_ENTROPY_MODE enumeration](..\webservices\ne-webservices-ws_security_key_entropy_mode.md) | Defines how randomness should be contributed to the issued key during a security token negotiation done with message and mixed-mode security. |
| [WS_SECURITY_KEY_HANDLE_TYPE enumeration](..\webservices\ne-webservices-ws_security_key_handle_type.md) | The types of security keys. |
| [WS_SECURITY_KEY_TYPE enumeration](..\webservices\ne-webservices-ws_security_key_type.md) | The key type of a security token. It is used as the return type when a security token is queried about its key. It is also used to specify the required key type when requesting a security token from a security token service. |
| [WS_SECURITY_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_security_property_id.md) | Identifies the properties representing channel-wide security settings. This enumeration is used within the WS_SECURITY_PROPERTY structure, which is in turn used within a WS_SECURITY_DESCRIPTION structure. |
| [WS_SECURITY_TIMESTAMP_USAGE enumeration](..\webservices\ne-webservices-ws_security_timestamp_usage.md) | With message security and mixed-mode security, this defines when a timestamp element should be generated and demanded in the WS-Security header. |
| [WS_SECURITY_TOKEN_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_security_token_property_id.md) | Defines the keys for the fields and properties that can be extracted from a security token. |
| [WS_SECURITY_TOKEN_REFERENCE_MODE enumeration](..\webservices\ne-webservices-ws_security_token_reference_mode.md) | With message and mixed-mode security bindings, the mechanism to use to refer to a security token from signatures, encrypted items and derived tokens. |
| [WS_SERVICE_CANCEL_REASON enumeration](..\webservices\ne-webservices-ws_service_cancel_reason.md) | The reasons for a cancellation. |
| [WS_SERVICE_ENDPOINT_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_service_endpoint_property_id.md) | Each property represents optional parameters for configuring the given WS_SERVICE_ENDPOINT structure. This enumeration is used within the WS_SERVICE_ENDPOINT_PROPERTY structure that is part of WS_SERVICE_ENDPOINT. |
| [WS_SERVICE_HOST_STATE enumeration](..\webservices\ne-webservices-ws_service_host_state.md) | The states that a service host can be in. |
| [WS_SERVICE_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_service_property_id.md) | The optional parameters for configuring the service host. This enumeration is used within the WS_SERVICE_PROPERTY structure when calling WsCreateServiceHost or by itself when calling WsGetServiceHostProperty. |
| [WS_SERVICE_PROXY_STATE enumeration](..\webservices\ne-webservices-ws_service_proxy_state.md) | The state of the service proxy. |
| [WS_TRACE_API enumeration](..\webservices\ne-webservices-ws_trace_api.md) | WS_TRACE_API enumeration |
| [WS_TRANSFER_MODE enumeration](..\webservices\ne-webservices-ws_transfer_mode.md) | Whether messages that are sent or received are streamed or buffered. |
| [WS_TRUST_VERSION enumeration](..\webservices\ne-webservices-ws_trust_version.md) | Defines the WS-Trust specification version to be used with message security and mixed-mode security. |
| [WS_TYPE enumeration](..\webservices\ne-webservices-ws_type.md) | The types supported for serialization. |
| [WS_TYPE_MAPPING enumeration](..\webservices\ne-webservices-ws_type_mapping.md) | How a WS_TYPE maps to or from XML when serialized or deserialized. |
| [WS_URL_SCHEME_TYPE enumeration](..\webservices\ne-webservices-ws_url_scheme_type.md) | The set of schemes used with WsDecodeUrl, WsEncodeUrl, and WsCombineUrl. |
| [WS_USERNAME_CREDENTIAL_TYPE enumeration](..\webservices\ne-webservices-ws_username_credential_type.md) | The type of the username/password credential, used as a selector for subtypes of WS_USERNAME_CREDENTIAL. |
| [WS_VALUE_TYPE enumeration](..\webservices\ne-webservices-ws_value_type.md) | The types of fixed-size primitives. |
| [WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL_TYPE enumeration](..\webservices\ne-webservices-ws_windows_integrated_auth_credential_type.md) | The type of the Windows Integrated Authentication credential, used as a selector for subtypes of WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL. |
| [WS_WINDOWS_INTEGRATED_AUTH_PACKAGE enumeration](..\webservices\ne-webservices-ws_windows_integrated_auth_package.md) | Defines the specific SSP package to be used for Windows Integrated Authentication. |
| [WS_WRITE_OPTION enumeration](..\webservices\ne-webservices-ws_write_option.md) | Specifies whether a storage specified contains the value, or a pointer to the value, and whether the value can be represented as nil in the XML content. |
| [WS_XML_BUFFER_PROPERTY_ID enumeration](..\webservices\ne-webservices-__unnamed_enum_0.md) | Each XML buffer property is identified by an ID and has an associated value. |
| [WS_XML_CANONICALIZATION_ALGORITHM enumeration](..\webservices\ne-webservices-ws_xml_canonicalization_algorithm.md) | The values for the XML canonicalization algorithms. |
| [WS_XML_CANONICALIZATION_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_xml_canonicalization_property_id.md) | Identifies each XML canonicalization property and its associated value. This enumeration is used within the WS_XML_CANONICALIZATION_PROPERTY structure, which is used as a parameter to WsStartReaderCanonicalization and WsStartWriterCanonicalization. |
| [WS_XML_NODE_TYPE enumeration](..\webservices\ne-webservices-ws_xml_node_type.md) | The type of WS_XML_NODE structure. |
| [WS_XML_READER_ENCODING_TYPE enumeration](..\webservices\ne-webservices-ws_xml_reader_encoding_type.md) | The type of WS_XML_READER_ENCODING structure. |
| [WS_XML_READER_INPUT_TYPE enumeration](..\webservices\ne-webservices-ws_xml_reader_input_type.md) | The type of WS_XML_READER_INPUT structure. |
| [WS_XML_READER_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_xml_reader_property_id.md) | Identifies each XML reader property is and its associated value. |
| [WS_XML_SECURITY_TOKEN_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_xml_security_token_property_id.md) | The keys for the bag of properties for the creation of XML security tokens. This enumeration is used within the WS_XML_SECURITY_TOKEN_PROPERTY structure, which is used as parameter for WsCreateXmlSecurityToken. |
| [WS_XML_TEXT_TYPE enumeration](..\webservices\ne-webservices-ws_xml_text_type.md) | The type of WS_XML_TEXT structure. |
| [WS_XML_WRITER_ENCODING_TYPE enumeration](..\webservices\ne-webservices-ws_xml_writer_encoding_type.md) | The type of WS_XML_WRITER_ENCODING structure. |
| [WS_XML_WRITER_OUTPUT_TYPE enumeration](..\webservices\ne-webservices-ws_xml_writer_output_type.md) | The type of WS_XML_WRITER_OUTPUT structure. |
| [WS_XML_WRITER_PROPERTY_ID enumeration](..\webservices\ne-webservices-ws_xml_writer_property_id.md) | Each xml writer property is identified by an ID and has an associated value. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IContentPrefetcherTaskTrigger interface](..\icontentprefetchertasktrigger\nn-icontentprefetchertasktrigger-icontentprefetchertasktrigger.md) | The IContentPrefetcherTaskTrigger interface supports content prefetching behavior and performance testing by defining methods that allow you to verify that an installed app package is registered for this background task and manually trigger its content prefetch operations. |

## Macros

| Title   | Description   |
| ---- |:---- |
| [WS_STRING_VALUE macro](..\webservices\nf-webservices-ws_string_value.md) | Initializes a WS_STRING structure given a constant string. |
| [WS_XML_STRING_DICTIONARY_VALUE macro](..\webservices\nf-webservices-ws_xml_string_dictionary_value.md) | Provides an initializer for a WS_XML_STRING structure when there is an associated dictionary ID. |
| [WS_XML_STRING_VALUE macro](..\webservices\nf-webservices-ws_xml_string_value.md) | Provides an initializer for a WS_XML_STRING structure when there is no associated dictionary ID. |
| [WsCountOf macro](..\webservices\nf-webservices-wscountof.md) | Returns the number of elements a specified array. |
| [WsOffsetOf macro](..\webservices\nf-webservices-wsoffsetof.md) | Returns the offset in bytes of a field within a structure given the names of the structure and field. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IContentPrefetcherTaskTrigger::IsRegisteredForContentPrefetch](..\icontentprefetchertasktrigger\nf-icontentprefetchertasktrigger-icontentprefetchertasktrigger-isregisteredforcontentprefetch.md) | Indicates if an app package has registered for the content prefetch background task. |
| [IContentPrefetcherTaskTrigger::TriggerContentPrefetcherTask](..\icontentprefetchertasktrigger\nf-icontentprefetchertasktrigger-icontentprefetchertasktrigger-triggercontentprefetchertask.md) | Triggers a content prefetch background task for the specified app package. |
