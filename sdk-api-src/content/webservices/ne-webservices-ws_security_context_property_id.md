---
UID: NE:webservices.WS_SECURITY_CONTEXT_PROPERTY_ID
title: WS_SECURITY_CONTEXT_PROPERTY_ID
author: windows-sdk-content
description: Identifies a property of a security context object. This enumeration is used with WsGetSecurityContextProperty.
old-location: wsw\ws_security_context_property_id.htm
old-project: wsw
ms.assetid: fd2b92d4-9834-4d4b-85c3-8ea8d2c8bd8c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_SECURITY_CONTEXT_PROPERTY_ID, WS_SECURITY_CONTEXT_PROPERTY_ID enumeration [Web Services for Windows], WS_SECURITY_CONTEXT_PROPERTY_IDENTIFIER, WS_SECURITY_CONTEXT_PROPERTY_MESSAGE_SECURITY_WINDOWS_TOKEN, WS_SECURITY_CONTEXT_PROPERTY_SAML_ASSERTION, WS_SECURITY_CONTEXT_PROPERTY_USERNAME, webservices/WS_SECURITY_CONTEXT_PROPERTY_ID, webservices/WS_SECURITY_CONTEXT_PROPERTY_IDENTIFIER, webservices/WS_SECURITY_CONTEXT_PROPERTY_MESSAGE_SECURITY_WINDOWS_TOKEN, webservices/WS_SECURITY_CONTEXT_PROPERTY_SAML_ASSERTION, webservices/WS_SECURITY_CONTEXT_PROPERTY_USERNAME, wsw.ws_security_context_property_id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: WS_SECURITY_CONTEXT_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SECURITY_CONTEXT_PROPERTY_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_SECURITY_CONTEXT_PROPERTY_ID enumeration


## -description


Identifies a property of a security context object.  This enumeration is used with <a href="https://msdn.microsoft.com/7ef32fbe-0b50-4ede-96af-075137df340d">WsGetSecurityContextProperty</a>.
      


## -enum-fields




### -field WS_SECURITY_CONTEXT_PROPERTY_IDENTIFIER

On the wire, a security context is identified by an absolute URI, which is unique to both sender and 
          recipient. See <a href="http://go.microsoft.com/fwlink/p/?linkid=131545">WS-SecureConversation</a>.
          This property is a <a href="https://msdn.microsoft.com/b9fd4497-153f-45f9-8f23-0771ffc47830">WS_UNIQUE_ID</a> structure that represents that URI.
        


### -field WS_SECURITY_CONTEXT_PROPERTY_USERNAME

If a <a href="https://msdn.microsoft.com/be6d4787-fa50-4260-8236-39dd992adcae">WS_USERNAME_MESSAGE_SECURITY_BINDING</a> is used as bootstrap security, this property
          is a <a href="https://msdn.microsoft.com/eb6c7397-6b15-4e79-89ec-585861113edf">WS_STRING</a> that represents the username that was used during the establishment of the security context.
        


### -field WS_SECURITY_CONTEXT_PROPERTY_MESSAGE_SECURITY_WINDOWS_TOKEN

If a <a href="https://msdn.microsoft.com/03127248-f5cc-44da-9c3d-abf016dd6bb2">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a> is used as bootstrap security, this property
          is a <b>HANDLE</b> that represents the token that was used during the establishment of the security context.
        


### -field WS_SECURITY_CONTEXT_PROPERTY_SAML_ASSERTION

If a <a href="https://msdn.microsoft.com/713afe9a-49b8-419a-b78b-d3b5a4a8d073">WS_SAML_MESSAGE_SECURITY_BINDING</a> is used as bootstrap security, this property
          is a pointer to a <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> that represents the SAML assertion that was used during the establishment of the security context.
        

