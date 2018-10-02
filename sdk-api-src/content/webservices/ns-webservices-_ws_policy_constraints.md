---
UID: NS:webservices._WS_POLICY_CONSTRAINTS
title: "_WS_POLICY_CONSTRAINTS"
author: windows-sdk-content
description: Specifies policy constraints for a channel.
old-location: wsw\ws_policy_constraints.htm
tech.root: wsw
ms.assetid: 2cf65426-336f-4148-ab3b-063a229db99f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_POLICY_CONSTRAINTS, WS_POLICY_CONSTRAINTS structure [Web Services for Windows], _WS_POLICY_CONSTRAINTS, webservices/WS_POLICY_CONSTRAINTS, wsw.ws_policy_constraints
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
 - WS_POLICY_CONSTRAINTS
product: Windows
targetos: Windows
req.typenames: WS_POLICY_CONSTRAINTS
req.redist: 
---

# _WS_POLICY_CONSTRAINTS structure


## -description


Specifies policy constraints for a channel.
            


## -struct-fields




### -field channelBinding

Which channel binding is required.  The
                    following values are supported:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_TCP_CHANNEL_BINDING</a>
</li>
</ul>

### -field channelPropertyConstraints

An array of channel property constraints which override the default
                    set of constraints.  The constraints specified here, combined
                    with the default set of constraints limits the set of policies
                    that will be matched.
                

If a channel property constraint is not specified for a given property,
                    then a default constraint value will be used.
                    See <a href="https://msdn.microsoft.com/548dcba5-dc78-402e-a930-a58fb462c08a">WS_CHANNEL_PROPERTY_CONSTRAINT</a> for the
                    supported set of properties and their default values.
                


### -field channelPropertyConstraintCount

The number of elements specified in the <b>channelPropertyConstraints</b>array.  
                

If this value is 0, then the channelPropertyConstraints array may be <b>NULL</b>.
                


### -field securityConstraints

Constraints on the type of security that may be used.
                

Setting this field to <b>NULL</b> indicates a constraint of no security.
                


### -field policyExtensions

 


### -field policyExtensionCount

 



