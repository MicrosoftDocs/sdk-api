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

# _WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT structure


## -description



                This structure is used to specify a set of constraints
                for a particular request security token property.
                Any property constraints that are not specified will use
                the default constraints.
            


## -struct-fields




### -field id


                    The id of the request security token property.  The following security
                    property constraint may be specified:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/7a2063eb-ab60-43d5-bd8c-41ef132abf50">WS_REQUEST_SECURITY_TOKEN_PROPERTY_TRUST_VERSION</a>

                        This property indicates which WS-Trust versions are acceptable.
                    


                        If this property is not specified, then the default constraint value
                        of <a href="https://msdn.microsoft.com/02a080f5-3d0d-4483-8215-bcb5b9f27b9c">WS_TRUST_VERSION_FEBRUARY_2005</a> will be used.
                    


                        Currently only <a href="https://msdn.microsoft.com/02a080f5-3d0d-4483-8215-bcb5b9f27b9c">WS_TRUST_VERSION_FEBRUARY_2005</a>
                        is supported in policy, so a property constraint containing the
                        value <b>WS_TRUST_VERSION_FEBRUARY_2005</b> must be specified in
                        order for the policy to match.
                    

</li>
</ul>

### -field allowedValues


                    An array of values which are acceptable.  The type of
                    the values in the array correspond to the type of the values
                    of the request security token property.  See the documentation for
                    a particular request security token property to determine the type of the
                    property.
                


### -field allowedValuesSize


                    The total size of the allowedValues array, in bytes.  This
                    size must be a multiple of the size of the type of the value
                    of the property.
                


### -field out


                    When <a href="https://msdn.microsoft.com/6e5f352b-5422-4bba-9525-7850bdddf0a5">WsMatchPolicyAlternative</a> returns NOERROR, the
                    entire contents of this structure will be filled out.
                


### -field out.requestSecurityTokenProperty

 



