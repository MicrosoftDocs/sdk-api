---
UID: NE:webservices.WS_SECURITY_TOKEN_PROPERTY_ID
title: WS_SECURITY_TOKEN_PROPERTY_ID
author: windows-sdk-content
description: Defines the keys for the fields and properties that can be extracted from a security token. Not all properties are valid for all security token types. The function WsGetSecurityTokenProperty uses the values defined here as keys.
old-location: wsw\ws_security_token_property_id.htm
tech.root: wsw
ms.assetid: d5ba0170-2345-4144-9a60-25c0e638a283
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_SECURITY_TOKEN_PROPERTY_ATTACHED_REFERENCE_XML, WS_SECURITY_TOKEN_PROPERTY_ID, WS_SECURITY_TOKEN_PROPERTY_ID enumeration [Web Services for Windows], WS_SECURITY_TOKEN_PROPERTY_KEY_TYPE, WS_SECURITY_TOKEN_PROPERTY_SERIALIZED_XML, WS_SECURITY_TOKEN_PROPERTY_SYMMETRIC_KEY, WS_SECURITY_TOKEN_PROPERTY_UNATTACHED_REFERENCE_XML, WS_SECURITY_TOKEN_PROPERTY_VALID_FROM_TIME, WS_SECURITY_TOKEN_PROPERTY_VALID_TILL_TIME, webservices/WS_SECURITY_TOKEN_PROPERTY_ATTACHED_REFERENCE_XML, webservices/WS_SECURITY_TOKEN_PROPERTY_ID, webservices/WS_SECURITY_TOKEN_PROPERTY_KEY_TYPE, webservices/WS_SECURITY_TOKEN_PROPERTY_SERIALIZED_XML, webservices/WS_SECURITY_TOKEN_PROPERTY_SYMMETRIC_KEY, webservices/WS_SECURITY_TOKEN_PROPERTY_UNATTACHED_REFERENCE_XML, webservices/WS_SECURITY_TOKEN_PROPERTY_VALID_FROM_TIME, webservices/WS_SECURITY_TOKEN_PROPERTY_VALID_TILL_TIME, wsw.ws_security_token_property_id
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
 - WS_SECURITY_TOKEN_PROPERTY_ID
product: Windows
targetos: Windows
req.typenames: WS_SECURITY_TOKEN_PROPERTY_ID
req.redist: 
---

# WS_SECURITY_TOKEN_PROPERTY_ID enumeration


## -description


Defines the keys for the fields and properties that can be extracted
from a security token.  Not all properties are valid for all security
token types.  The function <a href="https://msdn.microsoft.com/ce41062f-5125-4a4b-acc1-5df15b26276b">WsGetSecurityTokenProperty</a> uses
the values defined here as keys.
            

See also <a href="https://msdn.microsoft.com/f2790fd7-6f51-45a5-b2b6-e5aaaaca9660">WS_SECURITY_BINDING_PROPERTY</a>.
            


## -enum-fields




### -field WS_SECURITY_TOKEN_PROPERTY_KEY_TYPE

The accompanying <b>value</b> parameter of the <a href="https://msdn.microsoft.com/ce41062f-5125-4a4b-acc1-5df15b26276b">WsGetSecurityTokenProperty</a> function is a <a href="https://msdn.microsoft.com/95915a10-ba8f-41ca-89eb-777c85d2a411">WS_SECURITY_KEY_TYPE</a> value indicating the type of the proof key of the security token.


### -field WS_SECURITY_TOKEN_PROPERTY_VALID_FROM_TIME

The accompanying <b>value</b> parameter of the <a href="https://msdn.microsoft.com/ce41062f-5125-4a4b-acc1-5df15b26276b">WsGetSecurityTokenProperty</a> function is a <a href="https://msdn.microsoft.com/635f8e0b-f994-4500-85ad-dd74fb4a6c22">WS_DATETIME</a> structure containing the time from when the security token is valid.  For a security token
that does not define an explicit start time for its validity period, a
<b>WS_DATETIME</b> with a tick count of 0 is returned.


### -field WS_SECURITY_TOKEN_PROPERTY_VALID_TILL_TIME



The accompanying <b>value</b> parameter of the <a href="https://msdn.microsoft.com/ce41062f-5125-4a4b-acc1-5df15b26276b">WsGetSecurityTokenProperty</a> function is a <a href="https://msdn.microsoft.com/635f8e0b-f994-4500-85ad-dd74fb4a6c22">WS_DATETIME</a> structure containing the point in time at which a currently valid security token becomes invalid.  For a security token
that does not define an explicit end time for its validity period, a
<b>WS_DATETIME</b> with a tick count of 0 is returned.


### -field WS_SECURITY_TOKEN_PROPERTY_SERIALIZED_XML

The accompanying <b>value</b> parameter of the <a href="https://msdn.microsoft.com/ce41062f-5125-4a4b-acc1-5df15b26276b">WsGetSecurityTokenProperty</a> function is a pointer to a <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> containing the XML wire form of the security token.
                


### -field WS_SECURITY_TOKEN_PROPERTY_ATTACHED_REFERENCE_XML

The accompanying <b>value</b> parameter of the <a href="https://msdn.microsoft.com/ce41062f-5125-4a4b-acc1-5df15b26276b">WsGetSecurityTokenProperty</a> function is a pointer to a <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> containing
the XML wire form of the attached reference to the security token.
Attached references are used to refer to a security token when the
security token and its referring point (such as a signature using that
token) both occur in the same message.
                


### -field WS_SECURITY_TOKEN_PROPERTY_UNATTACHED_REFERENCE_XML

The accompanying <b>value</b> parameter of the <a href="https://msdn.microsoft.com/ce41062f-5125-4a4b-acc1-5df15b26276b">WsGetSecurityTokenProperty</a> function is a pointer to a <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> containing
the XML wire form of the unattached reference to the security token.
Unattached references are used to refer to a security token when the
security token does not occur in the same message as its referring
point (such as a signature using that token).
                


### -field WS_SECURITY_TOKEN_PROPERTY_SYMMETRIC_KEY

The accompanying <b>value</b> parameter of the <a href="https://msdn.microsoft.com/ce41062f-5125-4a4b-acc1-5df15b26276b">WsGetSecurityTokenProperty</a> function is a pointer to a <a href="https://msdn.microsoft.com/0106e372-80bf-4a62-b941-1a4501c92a9c">WS_BYTES</a> structure containing
                    the raw key data of the symmetric token key. This property is available when <a href="https://msdn.microsoft.com/d5ba0170-2345-4144-9a60-25c0e638a283">WS_SECURITY_TOKEN_PROPERTY_KEY_TYPE</a> is
                    <a href="https://msdn.microsoft.com/95915a10-ba8f-41ca-89eb-777c85d2a411">WS_SECURITY_KEY_TYPE_SYMMETRIC</a>.
                

If the token was obtained via <a href="https://msdn.microsoft.com/ee754a7d-73a9-49ae-afc7-b443fbbe0cce">WsRequestSecurityToken</a>, the returned buffer contains key material generated during 
                    the token request, which is either entropy generated by the client, entropy generated by the server or key material derived from from both client 
                    and server entropy, depending on <a href="https://msdn.microsoft.com/7a2063eb-ab60-43d5-bd8c-41ef132abf50">WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_ENTROPY</a>.
                

When using this property with <a href="https://msdn.microsoft.com/ce41062f-5125-4a4b-acc1-5df15b26276b">WsGetSecurityTokenProperty</a>, the 'heap' parameter must be non-NULL.
                

The returned buffer should be securely erased or encrypted immediately after use to prevent leaking of sensitive data.
            

