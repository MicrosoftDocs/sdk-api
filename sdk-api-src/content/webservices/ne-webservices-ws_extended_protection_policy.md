---
UID: NE:webservices.WS_EXTENDED_PROTECTION_POLICY
title: WS_EXTENDED_PROTECTION_POLICY
author: windows-sdk-content
description: Defines if Extended Protection data should be validated.
old-location: wsw\ws_extended_protection_policy.htm
old-project: wsw
ms.assetid: ee3685b1-0ffe-410e-a6fc-b31ed8d25b26
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_EXTENDED_PROTECTION_POLICY, WS_EXTENDED_PROTECTION_POLICY enumeration [Web Services for Windows], WS_EXTENDED_PROTECTION_POLICY_ALWAYS, WS_EXTENDED_PROTECTION_POLICY_NEVER, WS_EXTENDED_PROTECTION_POLICY_WHEN_SUPPORTED, webservices/WS_EXTENDED_PROTECTION_POLICY, webservices/WS_EXTENDED_PROTECTION_POLICY_ALWAYS, webservices/WS_EXTENDED_PROTECTION_POLICY_NEVER, webservices/WS_EXTENDED_PROTECTION_POLICY_WHEN_SUPPORTED, wsw.ws_extended_protection_policy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: v.1.0
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
tech.root: 
req.typenames: WS_EXTENDED_PROTECTION_POLICY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_EXTENDED_PROTECTION_POLICY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_EXTENDED_PROTECTION_POLICY enumeration


## -description


Defines if <a href="https://msdn.microsoft.com/35e48846-05e5-4db9-a3b5-098b62815b66">Extended Protection</a> data should be validated. This property is only available on the server,
                and can only be set when <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CHANNEL_BINDING</a> with <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> and either <a href="https://msdn.microsoft.com/03127248-f5cc-44da-9c3d-abf016dd6bb2">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>or <a href="https://msdn.microsoft.com/c6ca6760-a927-470f-9785-7500d1711902">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a> is used.
            


## -enum-fields




### -field WS_EXTENDED_PROTECTION_POLICY_NEVER

Extended protection data is not validated.
                


### -field WS_EXTENDED_PROTECTION_POLICY_WHEN_SUPPORTED

If the client system supports the extended protection feature, extended protection data is looked for and validated during authentication. Otherwise it is ignored.
                

A server can detect whether the client's operating system supports extended protection but chose not to include the extended protection data or 
                    whether it does not support extended protection. The former case is insecure and thus rejected. The latter is allowed when using this flag.
                

NOTE: If the client supports the extended protection feature, but did not include extended protection data in the authentication data, this setting will cause requests to fail. This 
                    scenario is possible when the operating system was patched but the client web services implementation does not send the neccessary data.
                

This is the default.
                


### -field WS_EXTENDED_PROTECTION_POLICY_ALWAYS

Extended protection data is required to be present and is always validated. Clients that are not extended-protection-aware cannot authenticate to a server 
                    setting this flag.
                

