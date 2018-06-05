---
UID: NS:webservices._WS_SECURITY_BINDING_PROPERTY_CONSTRAINT
title: "_WS_SECURITY_BINDING_PROPERTY_CONSTRAINT"
author: windows-sdk-content
description: This structure is used to specify a set of constraints for a particular security binding property. Any property constraints that are not specified will use the default constraints.
old-location: wsw\ws_security_binding_property_constraint.htm
old-project: wsw
ms.assetid: 97334ced-315d-49db-9c7b-b05ef387f6c8
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_SECURITY_BINDING_PROPERTY_CONSTRAINT, WS_SECURITY_BINDING_PROPERTY_CONSTRAINT structure [Web Services for Windows], _WS_SECURITY_BINDING_PROPERTY_CONSTRAINT, webservices/WS_SECURITY_BINDING_PROPERTY_CONSTRAINT, wsw.ws_security_binding_property_constraint
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
req.typenames: WS_SECURITY_BINDING_PROPERTY_CONSTRAINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_SECURITY_BINDING_PROPERTY_CONSTRAINT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_SECURITY_BINDING_PROPERTY_CONSTRAINT structure


## -description



                This structure is used to specify a set of constraints
                for a particular security binding property.
                Any property constraints that are not specified will use
                the default constraints.
            


## -struct-fields




### -field id


                    The id of the security binding property.  The following security
                    binding property constraints may be specified:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_SCHEME</a>

                      This property constraint may be specified when the
                      <a href="https://msdn.microsoft.com/198869b4-0f25-4f10-8740-e4d501f6791b">WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE</a>
                      security binding is specified.
                    

<ul>
<li>
<a href="https://msdn.microsoft.com/198869b4-0f25-4f10-8740-e4d501f6791b">WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE</a>
</li>
</ul>

                        If this property is not specified, then the default constraint value
                        of <a href="https://msdn.microsoft.com/c96e10ee-29d1-4c66-9f4d-64e663b25fd0">WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE</a> will be used.
                    

</li>
</ul>

### -field allowedValues


                    An array of values which are acceptable.  The type of
                    the values in the array correspond to the type of the values
                    of the security binding property.  See the documentation for
                    a particular security binding property to determine the type of the
                    property.
                


### -field allowedValuesSize


                    The total size of the allowedValues array, in bytes.  This
                    size must be a multiple of the size of the type of the value
                    of the property.
                


### -field out


                    When <a href="https://msdn.microsoft.com/6e5f352b-5422-4bba-9525-7850bdddf0a5">WsMatchPolicyAlternative</a> returns NOERROR, the
                    fields of the property structure will be filled out as follows:
                


### -field out.securityBindingProperty

 



