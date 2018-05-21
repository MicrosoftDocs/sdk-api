---
UID: NE:webservices.WS_PROXY_PROPERTY_ID
title: WS_PROXY_PROPERTY_ID
author: windows-driver-content
description: Optional parameters for configuring the service proxy. With an exception of WS_PROXY_PROPERTY_STATE all the values are only supported for use with WsCreateServiceProxy as part of the WS_PROXY_PROPERTY* parameter.
old-location: wsw\ws_proxy_property_id.htm
old-project: wsw
ms.assetid: d81944ae-74b9-4eee-b02f-5b1d5c99c358
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_PROXY_FAULT_LANG_ID, WS_PROXY_PROPERTY_CALL_TIMEOUT, WS_PROXY_PROPERTY_ID, WS_PROXY_PROPERTY_ID enumeration [Web Services for Windows], WS_PROXY_PROPERTY_MAX_CALL_POOL_SIZE, WS_PROXY_PROPERTY_MAX_CLOSE_TIMEOUT, WS_PROXY_PROPERTY_MAX_PENDING_CALLS, WS_PROXY_PROPERTY_MESSAGE_PROPERTIES, WS_PROXY_PROPERTY_STATE, webservices/WS_PROXY_FAULT_LANG_ID, webservices/WS_PROXY_PROPERTY_CALL_TIMEOUT, webservices/WS_PROXY_PROPERTY_ID, webservices/WS_PROXY_PROPERTY_MAX_CALL_POOL_SIZE, webservices/WS_PROXY_PROPERTY_MAX_CLOSE_TIMEOUT, webservices/WS_PROXY_PROPERTY_MAX_PENDING_CALLS, webservices/WS_PROXY_PROPERTY_MESSAGE_PROPERTIES, webservices/WS_PROXY_PROPERTY_STATE, wsw.ws_proxy_property_id
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
req.typenames: WS_PROXY_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_PROXY_PROPERTY_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_PROXY_PROPERTY_ID enumeration


## -description



                Optional parameters for configuring the service proxy. With an exception of
                <b>WS_PROXY_PROPERTY_STATE</b> all the values are only supported for 
                use with <a href="https://msdn.microsoft.com/9215684b-979e-48ad-b4ee-2ae1db1e3034">WsCreateServiceProxy</a> as part of the <a href="https://msdn.microsoft.com/eb8ce473-bf9e-4eae-8c40-8e2972a26d41">WS_PROXY_PROPERTY*</a> parameter. 
            


## -enum-fields




### -field WS_PROXY_PROPERTY_CALL_TIMEOUT


                    The maximum amount of time in milliseconds for a call to remain pending. 
                    Default is 30000 milliseconds(30 seconds).  It is of type <b>ULONG</b>.


                    If an application wishes to have no timeout associated with a call, it can set the value to INFINITE.
                


                    This property is write only.
                


### -field WS_PROXY_PROPERTY_MESSAGE_PROPERTIES


                    This property allows the user to specify properties of the message
                    objects used by the service proxy to send and receive messages.
                


                    This property may be specified when the service proxy is created.
                


                    The value specified should be of type <a href="https://msdn.microsoft.com/74ad74fd-457a-4408-8032-15d365f98b14">WS_MESSAGE_PROPERTIES</a>.
                


                    The following message properties may be specified:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_HEAP_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_XML_READER_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_XML_WRITER_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_MAX_PROCESSED_HEADERS</a>
</li>
</ul>

### -field WS_PROXY_PROPERTY_MAX_CALL_POOL_SIZE


                    Each call in the service proxy is represented by an object internal to the service proxy. 
                    A call object is designed such that after every call it can be reused. 
                    This allows applications to scale better in scenarios where they expect 
                    large number of calls over the service proxy. The default value for this property is 5.
                 It is of type <b>USHORT</b>.


                    This property is write only.
                


### -field WS_PROXY_PROPERTY_STATE


                    The current state of the service proxy.
                It is of type <a href="https://msdn.microsoft.com/82156e64-ae95-4a4a-aaad-e3dd69832c97">WS_SERVICE_PROXY_STATE</a>.


                    This property is read only.
                


                    The returned value is a snapshot of the current state, so it is
                    possible that the state may have changed before the caller has
                    had a chance to examine the value.
                


### -field WS_PROXY_PROPERTY_MAX_PENDING_CALLS


                    The maximum number of pending calls allowed on the service proxy. If the 
                    maximum number of calls pending on the service proxy reaches this limit, the
                    incoming calls will be rejected with <b>WS_E_QUOTA_EXCEEDED</b> (see <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>). The default value 
                    for this property is 100.
                 It is of type <b>ULONG</b>.


                    This property is write only.
                


### -field WS_PROXY_PROPERTY_MAX_CLOSE_TIMEOUT


                    The amount of time in milliseconds the service proxy will wait for the pending calls to complete.
                    Once the timeout expires, the service proxy will abort itself.
                


                    The default value for this property is 5000 (5 seconds).
                


                    This property is write only.
                 It is of type <b>ULONG</b>.


### -field WS_PROXY_FAULT_LANG_ID


                    The LANGID that would be used for returning a fault. If none specified default user locale will be used. It is of type <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">LANGID</a>. 
                


                    This property is write only.
                

