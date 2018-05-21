---
UID: NS:webservices._WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING
title: "_WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING"
author: windows-driver-content
description: The security binding subtype for specifying the use of a security context token negotiated between the client and server using WS-SecureConversation.
old-location: wsw\ws_security_context_message_security_binding.htm
old-project: wsw
ms.assetid: c7f45f44-25e9-4124-a0a2-eb9969f0eb99
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING, WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING structure [Web Services for Windows], _WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING, webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING, wsw.ws_security_context_message_security_binding
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING structure


## -description



The security binding subtype for specifying the use of a security context
token negotiated between the client and server using
WS-SecureConversation. This security binding may be used only with
message security. It is used to establish a message-level security
context. Another set of one or more security bindings, specified in the 
bootstrapSecurityDescription field, is used to the bootstrap the context.
            


            
            Only one instance of this binding may be present in a <a href="https://msdn.microsoft.com/b9490f00-877c-4d9f-b361-eaca343cdee0">security description</a>.
          This security binding is not supported with the <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_NAMEDPIPE_CHANNEL_BINDING</a>.
          


            When this binding is used, the channel must complete the receive of at least one 
            message before it can be used to send messages.            
          


With this security binding, the following security binding properties may be specified:
<ul>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_KEY_SIZE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_KEY_ENTROPY_MODE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_MESSAGE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_SECURE_CONVERSATION_VERSION</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_SUPPORT_RENEW</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_RENEWAL_INTERVAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_ROLLOVER_INTERVAL</a>
</li>
</ul>



## -struct-fields




### -field binding


The base type from which this security binding subtype and all other security binding subtypes derive.
                


### -field bindingUsage


            How the security token corresponding to this security binding should
            be attached to a message.
          


            Currently, only <a href="https://msdn.microsoft.com/2f19877f-b79b-43c3-a3f5-93dd2940d499">WS_SUPPORTING_MESSAGE_SECURITY_USAGE</a> is
            supported.  With this usage, this security binding provides client
            authentication, but not message protection (such as signing, encryption,
            replay detection).  Thus, this binding must be used together with
            another security binding such as the <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> 
            that provides a protected channel.
          


                To use this binding on HTTP without SSL, the security description property <b>WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL</b> must be explicitly set to <b>WS_PROTECTION_LEVEL_NONE</b>. This is not supported on the client or on TCP.


### -field bootstrapSecurityDescription


The security description for used to obtain the security context token.
                

