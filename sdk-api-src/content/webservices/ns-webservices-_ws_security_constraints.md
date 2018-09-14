---
UID: NS:webservices._WS_SECURITY_CONSTRAINTS
title: "_WS_SECURITY_CONSTRAINTS"
author: windows-sdk-content
description: This structure specifies the security related constraints as part of WS_POLICY_CONSTRAINTS.
old-location: wsw\ws_security_constraints.htm
tech.root: wsw
ms.assetid: 17fe7602-c050-46a2-b55c-aac6c277a5ce
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_SECURITY_CONSTRAINTS, WS_SECURITY_CONSTRAINTS structure [Web Services for Windows], _WS_SECURITY_CONSTRAINTS, webservices/WS_SECURITY_CONSTRAINTS, wsw.ws_security_constraints
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - WS_SECURITY_CONSTRAINTS
product: Windows
targetos: Windows
req.typenames: WS_SECURITY_CONSTRAINTS
req.redist: 
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
                    to the types of security that is specified using a <a href="https://msdn.microsoft.com/6c0663e8-ae73-41a2-9273-50f53534926b">WS_SECURITY_BINDING</a>structure.  Each security binding specifies one security token, and similarly,
                    each security binding constraint specifies constraints on one security token.
                

Specifying zero constraints indicates no security.
                


### -field securityBindingConstraintCount

The number of elements specified in the securityBindingConstraints
                    array.
                

If this value is 0, then the securityBindingConstraints array may be <b>NULL</b>.
                

