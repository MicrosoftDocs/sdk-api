---
UID: NS:webservices._WS_USERNAME_MESSAGE_SECURITY_BINDING
title: "_WS_USERNAME_MESSAGE_SECURITY_BINDING"
author: windows-sdk-content
description: The security binding subtype for specifying the use of an application supplied username / password pair as a direct (i.e., one-shot) security token.
old-location: wsw\ws_username_message_security_binding.htm
old-project: wsw
ms.assetid: be6d4787-fa50-4260-8236-39dd992adcae
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WS_USERNAME_MESSAGE_SECURITY_BINDING, WS_USERNAME_MESSAGE_SECURITY_BINDING structure [Web Services for Windows], _WS_USERNAME_MESSAGE_SECURITY_BINDING, webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING, wsw.ws_username_message_security_binding
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WS_USERNAME_MESSAGE_SECURITY_BINDING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_USERNAME_MESSAGE_SECURITY_BINDING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_USERNAME_MESSAGE_SECURITY_BINDING structure


## -description



The security binding subtype for specifying the use of an application
supplied username / password pair as a direct (i.e., one-shot)
security token.  This security binding may be used only with message
security.  It provides client authentication, but not traffic signing
or encryption.  So, it is used in conjunction with another transport
security or message security binding that provides message protection.
            


            Only one instance of this binding may be present in a <a href="https://msdn.microsoft.com/b9490f00-877c-4d9f-b361-eaca343cdee0">security description</a>.
          This security binding is not supported with the <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_NAMEDPIPE_CHANNEL_BINDING</a>.


With this security binding, no security binding properties may be specified.
            


## -struct-fields




### -field binding


The base type from which this security binding subtype and all other security binding subtypes derive.
                


### -field bindingUsage


How the security token corresponding to this security binding should be bound to a message.
                


                        Only <a href="https://msdn.microsoft.com/2f19877f-b79b-43c3-a3f5-93dd2940d499">WS_SUPPORTING_MESSAGE_SECURITY_USAGE</a> is
supported.  With this usage, this security binding provides client
authentication, but not message protection (such as signing, encryption,
replay detection).  Thus, this binding must be used together with
                        another security binding such as the <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> 
                        that provides a protected channel.



                    To use this binding on HTTP without SSL, the security description property <b>WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL</b> must be explicitly set to <b>WS_PROTECTION_LEVEL_NONE</b>. This is not supported on the client or on TCP.


### -field clientCredential


The username credential to be used with this security binding.  This
must be specified when this security binding is used on the
client.
                


### -field passwordValidator


The validator to be used to check received username/password pairs.
This must be specified when this security binding is used on the
service.

                


### -field passwordValidatorCallbackState


The optional state to be passed in as an argument when the username validator is invoked.
                

