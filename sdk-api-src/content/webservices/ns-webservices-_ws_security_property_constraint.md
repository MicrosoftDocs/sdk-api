---
UID: NS:webservices._WS_SECURITY_PROPERTY_CONSTRAINT
title: "_WS_SECURITY_PROPERTY_CONSTRAINT"
author: windows-sdk-content
description: This structure is used to specify a set of constraints for a particular security property. Any property constraints that are not specified will use the default constraints.
old-location: wsw\ws_security_property_constraint.htm
old-project: wsw
ms.assetid: 382d75be-2c56-44f5-8069-740ad9b9d1c4
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WS_SECURITY_PROPERTY_CONSTRAINT, WS_SECURITY_PROPERTY_CONSTRAINT structure [Web Services for Windows], _WS_SECURITY_PROPERTY_CONSTRAINT, webservices/WS_SECURITY_PROPERTY_CONSTRAINT, wsw.ws_security_property_constraint
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
tech.root: 
req.typenames: WS_SECURITY_PROPERTY_CONSTRAINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SECURITY_PROPERTY_CONSTRAINT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_SECURITY_PROPERTY_CONSTRAINT structure


## -description



                This structure is used to specify a set of constraints
                for a particular security property.
                Any property constraints that are not specified will use
                the default constraints.
            


## -struct-fields




### -field id


                    The id of the security property.  The following security
                    property constraints may be specified:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/98a824c9-11dd-4433-ae8f-2e6b6f6a520f">WS_SECURITY_PROPERTY_TIMESTAMP_USAGE</a>

                        This property constraint may be specified when any 
                        of the following security bindings are specified:
                    

<ul>
<li>
<a href="https://msdn.microsoft.com/a3003b9c-405e-4b3d-89a4-6c0884c28805">WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fd422ee4-64cd-464f-905f-b46b69e1a440">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/81f42654-8f94-4231-a798-67fbbe46e812">WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7abc37d8-cb00-459d-aa08-609a06b65a5c">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
</ul>

                        If this property is not specified, then the default constraint value
                        of <a href="https://msdn.microsoft.com/72e2a404-7988-40b8-b9ec-f9b9b3d767c1">WS_SECURITY_TIMESTAMP_USAGE_ALWAYS</a> will be used.
                    

</li>
<li>
<a href="https://msdn.microsoft.com/98a824c9-11dd-4433-ae8f-2e6b6f6a520f">WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL</a>

                        This property constraint may be specified when any
                        of the following security bindings are specified:
                    

<ul>
<li>
<a href="https://msdn.microsoft.com/1f547d95-0a9a-44c5-81db-b92880238b1d">WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c2e793dd-99a7-4028-9e08-4376d494e2b5">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1f6341b2-1f98-40a0-8f3a-cc9cf4538209">WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT</a>
</li>
</ul>

                        If this property is not specified, then the default constraint value
                        of <a href="https://msdn.microsoft.com/2b673728-1050-4005-bbb6-64b81ec19174">WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT</a> will be used.
                    
<b>WS_SECURITY_PROPERTY_SECURITY_HEADER_LAYOUT</b>
                        This property constraint may be specified when any
                        of the following security bindings are specified:
                    

<ul>
<li>
<a href="https://msdn.microsoft.com/a3003b9c-405e-4b3d-89a4-6c0884c28805">WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fd422ee4-64cd-464f-905f-b46b69e1a440">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/81f42654-8f94-4231-a798-67fbbe46e812">WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7abc37d8-cb00-459d-aa08-609a06b65a5c">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
</ul>

                        If this property is not specified, then the default constraint value
                        of <a href="https://msdn.microsoft.com/a3090e6f-1f80-4d67-b7d7-1165486dcc66">WS_SECURITY_HEADER_LAYOUT_STRICT</a> will be used.
                    
<b>WS_SECURITY_PROPERTY_SECURITY_HEADER_VERSION</b>
                        This property constraint may be specified when any
                        of the following security bindings are specified:
                    

<ul>
<li>
<a href="https://msdn.microsoft.com/a3003b9c-405e-4b3d-89a4-6c0884c28805">WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fd422ee4-64cd-464f-905f-b46b69e1a440">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/81f42654-8f94-4231-a798-67fbbe46e812">WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7abc37d8-cb00-459d-aa08-609a06b65a5c">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
</ul>

                        If this property is not specified, then the default constraint value
                        of <a href="https://msdn.microsoft.com/27093dc0-f4aa-4602-a51c-76633358792a">WS_SECURITY_HEADER_VERSION_1_1</a> will be used.
                    
<b>WS_SECURITY_PROPERTY_ALGORITHM_SUITE_NAME</b>
                    This property constraint may be specified when any
                    of the following security bindings are specified:
                  

<ul>
<li>
<a href="https://msdn.microsoft.com/a3003b9c-405e-4b3d-89a4-6c0884c28805">WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fd422ee4-64cd-464f-905f-b46b69e1a440">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/81f42654-8f94-4231-a798-67fbbe46e812">WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7abc37d8-cb00-459d-aa08-609a06b65a5c">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
</ul>

                    If this property is not specified, then the default constraint value
                    of <a href="https://msdn.microsoft.com/cd7116d2-86f6-475e-a55d-050c7e02172d">WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256</a> will be used.
                  

</li>
</ul>

### -field allowedValues


                    An array of values which are acceptable.  The type of
                    the values in the array correspond to the type of the values
                    of the security property.  See the documentation for
                    a particular security property to determine the type of the
                    property.
                


### -field allowedValuesSize


                    The total size of the allowedValues array, in bytes.  This
                    size must be a multiple of the size of the type of the value
                    of the property.
                


### -field out


                    When <a href="https://msdn.microsoft.com/6e5f352b-5422-4bba-9525-7850bdddf0a5">WsMatchPolicyAlternative</a> returns NOERROR, the
                    entire contents of this structure will be filled out.
                


### -field out.securityProperty

 



