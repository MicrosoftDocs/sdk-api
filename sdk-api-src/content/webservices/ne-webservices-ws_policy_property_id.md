---
UID: NE:webservices.WS_POLICY_PROPERTY_ID
title: WS_POLICY_PROPERTY_ID
author: windows-sdk-content
description: Identifies each policy property and its associated value.
old-location: wsw\ws_policy_property_id.htm
tech.root: wsw
ms.assetid: 503d39c0-7546-429d-b8e3-66e80c76b7c1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WS_POLICY_PROPERTY_ID, WS_POLICY_PROPERTY_ID enumeration [Web Services for Windows], WS_POLICY_PROPERTY_MAX_ALTERNATIVES, WS_POLICY_PROPERTY_MAX_DEPTH, WS_POLICY_PROPERTY_MAX_EXTENSIONS, WS_POLICY_PROPERTY_STATE, webservices/WS_POLICY_PROPERTY_ID, webservices/WS_POLICY_PROPERTY_MAX_ALTERNATIVES, webservices/WS_POLICY_PROPERTY_MAX_DEPTH, webservices/WS_POLICY_PROPERTY_MAX_EXTENSIONS, webservices/WS_POLICY_PROPERTY_STATE, wsw.ws_policy_property_id
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
 - WS_POLICY_PROPERTY_ID
product: Windows
targetos: Windows
req.typenames: WS_POLICY_PROPERTY_ID
req.redist: 
---

# WS_POLICY_PROPERTY_ID enumeration


## -description


Identifies each policy property and its associated
                value.
            


## -enum-fields




### -field WS_POLICY_PROPERTY_STATE

This property is used with <a href="https://msdn.microsoft.com/eebf1729-8492-47d3-90b2-6700d886de4a">WsGetPolicyProperty</a>.
                 It is of type <a href="https://msdn.microsoft.com/0f6252f4-ab99-4244-be77-92144eed4e3a">WS_POLICY_STATE</a>.

The current state of the policy object.


### -field WS_POLICY_PROPERTY_MAX_ALTERNATIVES

This property is used with <a href="https://msdn.microsoft.com/c3b6f926-331b-46a7-8180-36762abf63d7">WsCreateMetadata</a> when
                    specifying <a href="https://msdn.microsoft.com/d3baa961-4701-4f2f-9263-5ac0266f6056">WS_METADATA_PROPERTY_POLICY_PROPERTIES</a> as part of the <a href="https://msdn.microsoft.com/72c37aa9-f9d8-4fc5-8ad8-854e01cb54f4">WS_METADATA_PROPERTY*</a> parameter.  It is of type <b>ULONG</b>.
                

This property controls the maximum number of alternatives
                    allowed for a given <a href="https://msdn.microsoft.com/04623686-5065-4e97-8685-c72f848b92ab">WS_POLICY</a> object.
                

When a policy is processed, the amount of memory allocated 
                    and CPU consumed is proportional to the number of policy
                    alternatives present in the policy, not to the actual size
                    of the policy.  Even a small policy may contain a large number
                    of alternatives due to the expansion of different permutations
                    of assertions.  Setting this property to a large
                    value may lead to excessive processing or memory consumption.
                

The default value is 32.
                


### -field WS_POLICY_PROPERTY_MAX_DEPTH

This property is used with <a href="https://msdn.microsoft.com/c3b6f926-331b-46a7-8180-36762abf63d7">WsCreateMetadata</a> when
                    specifying <a href="https://msdn.microsoft.com/d3baa961-4701-4f2f-9263-5ac0266f6056">WS_METADATA_PROPERTY_POLICY_PROPERTIES</a>.
                  It is of type <b>ULONG</b>.

This property controls the maximum depth of any policy that is
                    read and processed.  The maximum depth of a policy is defined as the maximum
                    number of levels of nested container elements (<b>Policy</b>, <b>All</b>, <b>ExactlyOne</b>)
                    when considering the policy and any policies that it references.
                

A small amount of stack space is consumed for each level of
                    policy that is processed.  Setting this value to a large
                    value may lead to stack overflow for a policy that is 
                    deeply nested or contains a cyclic reference.
                

The default value is 32.
                


### -field WS_POLICY_PROPERTY_MAX_EXTENSIONS

This property is used with <a href="https://msdn.microsoft.com/c3b6f926-331b-46a7-8180-36762abf63d7">WsCreateMetadata</a> when
                    specifying <a href="https://msdn.microsoft.com/d3baa961-4701-4f2f-9263-5ac0266f6056">WS_METADATA_PROPERTY_POLICY_PROPERTIES</a>.
                 It is of type <b>ULONG</b>.

This property controls the maximum number of policy extensions 
                    (unknown assertions) allowed for a given <a href="https://msdn.microsoft.com/04623686-5065-4e97-8685-c72f848b92ab">WS_POLICY</a> object. 
                    Policy extensions can be retrieved by supplying <a href="https://msdn.microsoft.com/85a3fa35-b574-4091-9ef2-486ac751ef82">WS_POLICY_EXTENSION</a> 
                    array in <a href="https://msdn.microsoft.com/2cf65426-336f-4148-ab3b-063a229db99f">WS_POLICY_CONSTRAINTS</a> structure when using the 
                    <a href="https://msdn.microsoft.com/6e5f352b-5422-4bba-9525-7850bdddf0a5">WsMatchPolicyAlternative</a> API.
                

The default value is 8.
                

When a policy is processed, the amount of memory allocated 
                    and CPU consumed is porportional to the number of policy
                    alternatives present in the policy, not to the actual size
                    of the policy.  Even a small policy may contain a large number
                    of alternatives due to the expansion of different permutations
                    of assertions.  Setting this property to a large
                    value may lead to excessive processing or memory consumption.
                

