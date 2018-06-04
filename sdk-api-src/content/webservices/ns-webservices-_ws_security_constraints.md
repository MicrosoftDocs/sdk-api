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

# _WS_SECURITY_CONSTRAINTS structure


## -description



                This structure specifies the security related constraints
                as part of <a href="https://msdn.microsoft.com/2cf65426-336f-4148-ab3b-063a229db99f">WS_POLICY_CONSTRAINTS</a>.
            


## -struct-fields




### -field securityPropertyConstraints


                    An array of security property constraints which override the default
                    set of constraints.  The constraints specified here, combined
                    with the default set of constraints limits the set of policies
                    that will be matched.
                


                    If a security property constraint is not specified for a given property,
                    then a default constraint value will be used.
                    See <a href="https://msdn.microsoft.com/382d75be-2c56-44f5-8069-740ad9b9d1c4">WS_SECURITY_PROPERTY_CONSTRAINT</a> for the
                    supported set of properties and their default values.
                


                    Note that the defaults constraints for <a href="https://msdn.microsoft.com/382d75be-2c56-44f5-8069-740ad9b9d1c4">WS_SECURITY_PROPERTY_CONSTRAINT</a> 
                    are the same as the defaults for <a href="https://msdn.microsoft.com/676079cd-6ca8-486b-9604-172423210ad5">WS_SECURITY_PROPERTY</a>.
                


### -field securityPropertyConstraintCount


                    The number of elements specified in the securityPropertyConstraints
                    array.
                


                    If this value is 0, then the securityPropertyConstraints array may be <b>NULL</b>.
                


### -field securityBindingConstraints


                    Any array of security binding constraints which taken as a unit specify
                    the type of security to match in the policy.
                


                    The type of each <a href="https://msdn.microsoft.com/d79795ea-6780-4d13-9d40-bd1ea7cd5113">WS_SECURITY_BINDING_CONSTRAINT</a> corresponds
                    to the types of security that is specified using a <a href="https://msdn.microsoft.com/6c0663e8-ae73-41a2-9273-50f53534926b">WS_SECURITY_BINDING</a>
                    structure.  Each security binding specifies one security token, and similarly,
                    each security binding constraint specifies constraints on one security token.
                


                    Specifying zero constraints indicates no security.
                


### -field securityBindingConstraintCount


                    The number of elements specified in the securityBindingConstraints
                    array.
                


                    If this value is 0, then the securityBindingConstraints array may be <b>NULL</b>.
                

