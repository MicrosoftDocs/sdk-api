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


                    The number of elements specified in the <b>channelPropertyConstraints</b>
                    array.  
                


                    If this value is 0, then the channelPropertyConstraints array may be <b>NULL</b>.
                


### -field securityConstraints


                    Constraints on the type of security that may be used.
                


                    Setting this field to <b>NULL</b> indicates a constraint of no security.
                


### -field policyExtensions

 


### -field policyExtensionCount

 



