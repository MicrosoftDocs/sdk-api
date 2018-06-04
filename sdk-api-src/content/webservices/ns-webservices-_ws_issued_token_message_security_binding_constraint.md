---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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



