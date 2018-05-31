---
UID: TP:dataxchg
ms.assetid: 8367a3cd-5a5f-3203-9e68-d3a9a508c968
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Data Exchange



Overview of the Data Exchange technology.

To develop Data Exchange, you need these headers:

 * [dde.h](..\dde\index.md)
 * [ddeml.h](..\ddeml\index.md)
 * [wingdi.h](..\wingdi\index.md)

For the programming guide, see [Data Exchange](/windows/desktop/dataxchg).

## Functions

| Title   | Description   |
| ---- |:---- |
| [DdeAbandonTransaction function](..\ddeml\nf-ddeml-ddeabandontransaction.md) | Abandons the specified asynchronous transaction and releases all resources associated with the transaction. |
| [DdeAccessData function](..\ddeml\nf-ddeml-ddeaccessdata.md) | Provides access to the data in the specified Dynamic Data Exchange (DDE) object. An application must call the DdeUnaccessData function when it has finished accessing the data in the object. |
| [DdeAddData function](..\ddeml\nf-ddeml-ddeadddata.md) | Adds data to the specified Dynamic Data Exchange (DDE) object. |
| [DdeClientTransaction function](..\ddeml\nf-ddeml-ddeclienttransaction.md) | Begins a data transaction between a client and a server. Only a Dynamic Data Exchange (DDE) client application can call this function, and the application can use it only after establishing a conversation with the server. |
| [DdeCmpStringHandles function](..\ddeml\nf-ddeml-ddecmpstringhandles.md) | Compares the values of two string handles. The value of a string handle is not related to the case of the associated string. |
| [DdeConnect function](..\ddeml\nf-ddeml-ddeconnect.md) | Establishes a conversation with a server application that supports the specified service name and topic name pair. If more than one such server exists, the system selects only one. |
| [DdeConnectList function](..\ddeml\nf-ddeml-ddeconnectlist.md) | Establishes a conversation with all server applications that support the specified service name and topic name pair. |
| [DdeCreateDataHandle function](..\ddeml\nf-ddeml-ddecreatedatahandle.md) | Creates a Dynamic Data Exchange (DDE) object and fills the object with data from the specified buffer. A DDE application uses this function during transactions that involve passing data to the partner application. |
| [DdeCreateStringHandleA function](..\ddeml\nf-ddeml-ddecreatestringhandlea.md) | Creates a handle that identifies the specified string. A Dynamic Data Exchange (DDE) client or server application can pass the string handle as a parameter to other Dynamic Data Exchange Management Library (DDEML) functions. |
| [DdeCreateStringHandleW function](..\ddeml\nf-ddeml-ddecreatestringhandlew.md) | Creates a handle that identifies the specified string. A Dynamic Data Exchange (DDE) client or server application can pass the string handle as a parameter to other Dynamic Data Exchange Management Library (DDEML) functions. |
| [DdeDisconnect function](..\ddeml\nf-ddeml-ddedisconnect.md) | Terminates a conversation started by either the DdeConnect or DdeConnectList function and invalidates the specified conversation handle. |
| [DdeDisconnectList function](..\ddeml\nf-ddeml-ddedisconnectlist.md) | Destroys the specified conversation list and terminates all conversations associated with the list. |
| [DdeEnableCallback function](..\ddeml\nf-ddeml-ddeenablecallback.md) | Enables or disables transactions for a specific conversation or for all conversations currently established by the calling application. |
| [DdeFreeDataHandle function](..\ddeml\nf-ddeml-ddefreedatahandle.md) | Frees a Dynamic Data Exchange (DDE) object and deletes the data handle associated with the object. |
| [DdeFreeStringHandle function](..\ddeml\nf-ddeml-ddefreestringhandle.md) | Frees a string handle in the calling application. |
| [DdeGetData function](..\ddeml\nf-ddeml-ddegetdata.md) | Copies data from the specified Dynamic Data Exchange (DDE) object to the specified local buffer. |
| [DdeGetLastError function](..\ddeml\nf-ddeml-ddegetlasterror.md) | Retrieves the most recent error code set by the failure of a Dynamic Data Exchange Management Library (DDEML) function and resets the error code to DMLERR_NO_ERROR. |
| [DdeImpersonateClient function](..\ddeml\nf-ddeml-ddeimpersonateclient.md) | Impersonates a Dynamic Data Exchange (DDE) client application in a DDE client conversation. |
| [DdeInitializeA function](..\ddeml\nf-ddeml-ddeinitializea.md) | Registers an application with the Dynamic Data Exchange Management Library (DDEML). An application must call this function before calling any other Dynamic Data Exchange Management Library (DDEML) function. |
| [DdeInitializeW function](..\ddeml\nf-ddeml-ddeinitializew.md) | Registers an application with the Dynamic Data Exchange Management Library (DDEML). An application must call this function before calling any other Dynamic Data Exchange Management Library (DDEML) function. |
| [DdeKeepStringHandle function](..\ddeml\nf-ddeml-ddekeepstringhandle.md) | Increments the usage count associated with the specified handle. |
| [DdeNameService function](..\ddeml\nf-ddeml-ddenameservice.md) | Registers or unregisters the service names a Dynamic Data Exchange (DDE) server supports. |
| [DdePostAdvise function](..\ddeml\nf-ddeml-ddepostadvise.md) | Causes the system to send an XTYP_ADVREQ transaction to the calling (server) application's Dynamic Data Exchange (DDE) callback function for each client with an active advise loop on the specified topic and item. |
| [DdeQueryConvInfo function](..\ddeml\nf-ddeml-ddequeryconvinfo.md) | Retrieves information about a Dynamic Data Exchange (DDE) transaction and about the conversation in which the transaction takes place. |
| [DdeQueryNextServer function](..\ddeml\nf-ddeml-ddequerynextserver.md) | Retrieves the next conversation handle in the specified conversation list. |
| [DdeQueryStringA function](..\ddeml\nf-ddeml-ddequerystringa.md) | Copies text associated with a string handle into a buffer. |
| [DdeQueryStringW function](..\ddeml\nf-ddeml-ddequerystringw.md) | Copies text associated with a string handle into a buffer. |
| [DdeReconnect function](..\ddeml\nf-ddeml-ddereconnect.md) | Enables a client Dynamic Data Exchange Management Library (DDEML) application to attempt to reestablish a conversation with a service that has terminated a conversation with the client. |
| [DdeSetQualityOfService function](..\dde\nf-dde-ddesetqualityofservice.md) | Specifies the quality of service (QOS) a raw Dynamic Data Exchange (DDE) application desires for future DDE conversations it initiates. |
| [DdeSetUserHandle function](..\ddeml\nf-ddeml-ddesetuserhandle.md) | Associates an application-defined value with a conversation handle or a transaction identifier. This is useful for simplifying the processing of asynchronous transactions. An application can use the DdeQueryConvInfo function to retrieve this value. |
| [DdeUnaccessData function](..\ddeml\nf-ddeml-ddeunaccessdata.md) | Unaccesses a Dynamic Data Exchange (DDE) object. An application must call this function after it has finished accessing the object. |
| [DdeUninitialize function](..\ddeml\nf-ddeml-ddeuninitialize.md) | Frees all Dynamic Data Exchange Management Library (DDEML) resources associated with the calling application. |
| [FreeDDElParam function](..\dde\nf-dde-freeddelparam.md) | Frees the memory specified by the lParam parameter of a posted Dynamic Data Exchange (DDE) message. An application receiving a posted DDE message should call this function after it has used the UnpackDDElParam function to unpack the lParam value. |
| [ImpersonateDdeClientWindow function](..\dde\nf-dde-impersonateddeclientwindow.md) | Enables a Dynamic Data Exchange (DDE) server application to impersonate a DDE client application's security context. This protects secure server data from unauthorized DDE clients. |
| [PackDDElParam function](..\dde\nf-dde-packddelparam.md) | Packs a Dynamic Data Exchange (DDE) lParam value into an internal structure used for sharing DDE data between processes. |
| [ReuseDDElParam function](..\dde\nf-dde-reuseddelparam.md) | Enables an application to reuse a packed Dynamic Data Exchange (DDE) lParam parameter, rather than allocating a new packed lParam. Using this function reduces reallocations for applications that pass packed DDE messages. |
| [UnpackDDElParam function](..\dde\nf-dde-unpackddelparam.md) | Unpacks a Dynamic Data Exchange (DDE)lParam value received from a posted DDE message. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [DDEACK structure](..\dde\ns-dde-ddeack.md) | Contains status flags that a DDE application passes to its partner as part of the WM_DDE_ACK message. |
| [DDEADVISE structure](..\dde\ns-dde-ddeadvise.md) | Contains flags that specify how a DDE server application should send data to a client application during an advise loop. A client passes a handle to a DDEADVISE structure to a server as part of a WM_DDE_ADVISE message. |
| [DDEDATA structure](..\dde\ns-dde-ddedata.md) | Contains the data, and information about the data, sent as part of a WM_DDE_DATA message. |
| [DDEPOKE structure](..\dde\ns-dde-ddepoke.md) | Contains the data, and information about the data, sent as part of a WM_DDE_POKE message. |
| [tagCONVCONTEXT structure](..\ddeml\ns-ddeml-tagconvcontext.md) | Contains information supplied by a Dynamic Data Exchange (DDE) client application. The information is useful for specialized or cross-language DDE conversations. |
| [tagCONVINFO structure](..\ddeml\ns-ddeml-tagconvinfo.md) | Contains information about a Dynamic Data Exchange (DDE) conversation. |
| [tagDDEML_MSG_HOOK_DATA structure](..\ddeml\ns-ddeml-tagddeml_msg_hook_data.md) | Contains information about a Dynamic Data Exchange (DDE) message, and provides read access to the data referenced by the message. This structure is intended to be used by a Dynamic Data Exchange Management Library (DDEML) monitoring application. |
| [tagHSZPAIR structure](..\ddeml\ns-ddeml-taghszpair.md) | Contains a DDE service name and topic name. A DDE server application can use this structure during an XTYP_WILDCONNECT transaction to enumerate the service-topic pairs that it supports. |
| [tagMETAFILEPICT structure](..\wingdi\ns-wingdi-tagmetafilepict.md) | Defines the metafile picture format used for exchanging metafile data through the clipboard. |
| [tagMONCBSTRUCT structure](..\ddeml\ns-ddeml-tagmoncbstruct.md) | Contains information about the current Dynamic Data Exchange (DDE) transaction. A DDE debugging application can use this structure when monitoring transactions that the system passes to the DDE callback functions of other applications. |
| [tagMONCONVSTRUCT structure](..\ddeml\ns-ddeml-tagmonconvstruct.md) | Contains information about a Dynamic Data Exchange (DDE) conversation. A DDE monitoring application can use this structure to obtain information about a conversation that has been established or has terminated. |
| [tagMONERRSTRUCT structure](..\ddeml\ns-ddeml-tagmonerrstruct.md) | Contains information about the current Dynamic Data Exchange (DDE) error. A DDE monitoring application can use this structure to monitor errors returned by DDE Management Library functions. |
| [tagMONHSZSTRUCTA structure](..\ddeml\ns-ddeml-tagmonhszstructa.md) | Contains information about a Dynamic Data Exchange (DDE) string handle. A DDE monitoring application can use this structure when monitoring the activity of the string manager component of the DDE Management Library. |
| [tagMONHSZSTRUCTW structure](..\ddeml\ns-ddeml-tagmonhszstructw.md) | Contains information about a Dynamic Data Exchange (DDE) string handle. A DDE monitoring application can use this structure when monitoring the activity of the string manager component of the DDE Management Library. |
| [tagMONLINKSTRUCT structure](..\ddeml\ns-ddeml-tagmonlinkstruct.md) | Contains information about a Dynamic Data Exchange (DDE) advise loop. A DDE monitoring application can use this structure to obtain information about an advise loop that has started or ended. |
| [tagMONMSGSTRUCT structure](..\ddeml\ns-ddeml-tagmonmsgstruct.md) | Contains information about a Dynamic Data Exchange (DDE) message. A DDE monitoring application can use this structure to obtain information about a DDE message that was sent or posted. |
