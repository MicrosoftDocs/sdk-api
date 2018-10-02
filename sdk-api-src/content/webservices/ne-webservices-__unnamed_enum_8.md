---
UID: NE:webservices.__unnamed_enum_8
title: "__unnamed_enum_8"
author: windows-sdk-content
description: Defines failures related to certificate validation. Can be used with WS_SECURITY_BINDING_PROPERTY_CERT_FAILURES_TO_IGNORE to specify which certificate verification failures should be ignored.
old-location: wsw\ws_cert_failure.htm
tech.root: wsw
ms.assetid: e2324688-abf5-4b09-b236-502af8e1fcd1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_CERT_FAILURE, WS_CERT_FAILURE enumeration [Web Services for Windows], WS_CERT_FAILURE_CN_MISMATCH, WS_CERT_FAILURE_INVALID_DATE, WS_CERT_FAILURE_REVOCATION_OFFLINE, WS_CERT_FAILURE_UNTRUSTED_ROOT, WS_CERT_FAILURE_WRONG_USAGE, __unnamed_enum_8, webservices/WS_CERT_FAILURE, webservices/WS_CERT_FAILURE_CN_MISMATCH, webservices/WS_CERT_FAILURE_INVALID_DATE, webservices/WS_CERT_FAILURE_REVOCATION_OFFLINE, webservices/WS_CERT_FAILURE_UNTRUSTED_ROOT, webservices/WS_CERT_FAILURE_WRONG_USAGE, wsw.ws_cert_failure
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_CERT_FAILURE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# __unnamed_enum_8 enumeration


## -description


Defines failures related to certificate validation. Can be used with <a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_CERT_FAILURES_TO_IGNORE</a> to 
                specify which certificate verification failures should be ignored.
            


## -enum-fields




### -field WS_CERT_FAILURE_CN_MISMATCH

Failure due to a certificate that contains a common name that does not match the server name specified by the application.
                    
                    When used with <a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_CERT_FAILURES_TO_IGNORE</a>, this flag will suppress the <b>CERT_E_CN_NO_MATCH</b> error code. (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)
                


### -field WS_CERT_FAILURE_INVALID_DATE

Failure due to an expired or not-yet-effective certificate.
                    
                    When used with <a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_CERT_FAILURES_TO_IGNORE</a>, this flag will suppress the <b>CERT_E_EXPIRED</b> error code.
                


### -field WS_CERT_FAILURE_UNTRUSTED_ROOT

Failure due to the root certificate of the certificate chain being untrusted.
                    
                    When used with <a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_CERT_FAILURES_TO_IGNORE</a>, this flag will suppress the <b>CERT_E_UNTRUSTEDROOT</b> error code.
                


### -field WS_CERT_FAILURE_WRONG_USAGE

Failure due to the server using a non-server certificate to establish its identity.
                    
                    When used with <a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_CERT_FAILURES_TO_IGNORE</a>, this flag will suppress the <b>CERT_E_WRONG_USAGE</b> error code.
                


### -field WS_CERT_FAILURE_REVOCATION_OFFLINE

Failure due to the certificate revocation server being offline.
                    
                    When used with <a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_CERT_FAILURES_TO_IGNORE</a>, this flag will cause the channel 
                    to intercept the <b>CRYPT_E_REVOCATION_OFFLINE</b> error code and resend the request without certificate revocation checking.
                

