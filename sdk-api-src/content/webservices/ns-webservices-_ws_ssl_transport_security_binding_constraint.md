---
UID: NS:webservices._WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT
title: "_WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT"
author: windows-sdk-content
description: A security binding constraint that corresponds to the WS_SSL_TRANSPORT_SECURITY_BINDING.
old-location: wsw\ws_ssl_transport_security_binding_constraint.htm
old-project: wsw
ms.assetid: 1f547d95-0a9a-44c5-81db-b92880238b1d
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT, WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT structure [Web Services for Windows], _WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT, webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT, wsw.ws_ssl_transport_security_binding_constraint
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
req.typenames: WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT structure


## -description



                A security binding constraint that corresponds to the 
                <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a>.
            


## -struct-fields




### -field bindingConstraint


                    The base binding constraint that this binding constraint derives from.
                


                    There are no binding-specific properties are defined for this binding constraint
                    at this time.
                


### -field out


                    When <a href="https://msdn.microsoft.com/6e5f352b-5422-4bba-9525-7850bdddf0a5">WsMatchPolicyAlternative</a> returns NOERROR, the
                    entire contents of this structure will be filled out.
                


### -field out.clientCertCredentialRequired

 



