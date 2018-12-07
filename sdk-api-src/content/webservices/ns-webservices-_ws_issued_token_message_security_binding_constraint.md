---
UID: NS:webservices._WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT
title: "_WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT"
author: windows-sdk-content
description: A security binding constraint that can be used to extract information about how to obtain an issued token from an issuing party.
old-location: wsw\ws_issued_token_message_security_binding_constraint.htm
tech.root: wsw
ms.assetid: 7588f526-d1d5-486f-b317-f1a4b35e3882
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT, WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT structure [Web Services for Windows], _WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT, webservices/WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT, wsw.ws_issued_token_message_security_binding_constraint
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
 - WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT
product: Windows
targetos: Windows
req.typenames: WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT
req.redist: 
---

# _WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT structure


## -description


A security binding constraint that can be used to extract information
                about how to obtain an issued token from an issuing party.
            


## -struct-fields




### -field bindingConstraint

The base binding constraint that this binding constraint derives from.
                

There are currently no binding-specific properties defined for this binding constraint.
                


### -field bindingUsage

This specifies how the issued token should be attached to a message.
                


### -field claimConstraints

This field contains a list of claim types that 
                    are allowed in the policy.  Each claim type is 
                    a URI which identifies the type of claim.
                


### -field claimConstraintCount

The number of elements in the claimConstraints array.
                

If this value is 0, then the claimConstraints array may be
                    <b>NULL</b>, and any claims are allowed to appear in the policy.
                


### -field requestSecurityTokenPropertyConstraints

A set of property constraints relating to how to request a security token.
                

See <a href="https://msdn.microsoft.com/96bd488f-ef28-402a-ae55-a30416f4e103">WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT</a> for more information.
                


### -field requestSecurityTokenPropertyConstraintCount

The number of elements in the requestSecurityTokenPropertyConstraints array.
                

If the array has zero elements, the requestSecurityTokenPropertyConstraints field may be <b>NULL</b>.
                


### -field out

When <a href="https://msdn.microsoft.com/6e5f352b-5422-4bba-9525-7850bdddf0a5">WsMatchPolicyAlternative</a> returns NOERROR, the
                    entire contents of this structure will be filled out.
                


### -field out.issuerAddress

 


### -field out.requestSecurityTokenTemplate

 




## -remarks



The information extracted using this binding constraint can be used
                with <a href="https://msdn.microsoft.com/ee754a7d-73a9-49ae-afc7-b443fbbe0cce">WsRequestSecurityToken</a> to obtain an issued token.
                The issued token can then be used with the 
                <a href="https://msdn.microsoft.com/5ca1e67a-11f5-44bb-afe8-c934837d711b">WS_XML_TOKEN_MESSAGE_SECURITY_BINDING</a> security binding.
            

This binding constraint is typically used in federated security
                scenarios.  



