---
UID: NS:webservices._WS_CHANNEL_PROPERTY_CONSTRAINT
title: "_WS_CHANNEL_PROPERTY_CONSTRAINT"
author: windows-sdk-content
description: Specifies constraints for a particular channel property.
old-location: wsw\ws_channel_property_constraint.htm
old-project: wsw
ms.assetid: 548dcba5-dc78-402e-a930-a58fb462c08a
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WS_CHANNEL_PROPERTY_CONSTRAINT, WS_CHANNEL_PROPERTY_CONSTRAINT structure [Web Services for Windows], _WS_CHANNEL_PROPERTY_CONSTRAINT, webservices/WS_CHANNEL_PROPERTY_CONSTRAINT, wsw.ws_channel_property_constraint
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
req.typenames: WS_CHANNEL_PROPERTY_CONSTRAINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_CHANNEL_PROPERTY_CONSTRAINT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_CHANNEL_PROPERTY_CONSTRAINT structure


## -description


Specifies constraints
                for a particular channel property.
                Any property constraints that are not specified will use
                the default constraints.
            


## -struct-fields




### -field id


                    The ID of the channel property.  The following channel 
                    properties constraints may be specified:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_ENCODING</a>

                        If this property constraint is not specified when using 
                        <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a> the default constraint value
                        of <a href="https://msdn.microsoft.com/37858df7-ae76-41c1-8fd2-fc810b8927bf">WS_ENCODING_XML_UTF8</a> will be used.
                    


                        If this property constraint is not specified not specified when using 
                        <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_TCP_CHANNEL_BINDING</a> the default constraint value of 
                        <a href="https://msdn.microsoft.com/37858df7-ae76-41c1-8fd2-fc810b8927bf">WS_ENCODING_XML_BINARY_SESSION_1</a> will be used.
                    

</li>
<li>
<a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_ADDRESSING_VERSION</a>

                        If this property constraint is not specified, the default constraint
                        value of <a href="https://msdn.microsoft.com/87f60067-109c-456c-b060-33ab840872e0">WS_ADDRESSING_VERSION_1_0</a> will be used.
                    

</li>
<li>
<a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_ENVELOPE_VERSION</a>

                        If this property constraint is not specified, the default constraint of 
                        value of <a href="https://msdn.microsoft.com/2a6f6148-d37d-4ac2-8fd0-409eae71a3d8">WS_ENVELOPE_VERSION_SOAP_1_2</a> will be used.
                    

</li>
</ul>

### -field allowedValues


                    An array of acceptable values.  The type of
                    the values in the array correspond to the type of the values
                    of the channel property.  See the documentation for
                    a particular channel property to determine the type of the
                    property.
                


### -field allowedValuesSize


                    The total size of the <b>allowedValues</b> array, in bytes.  This
                    size must be a multiple of the size of the type of the value
                    of the property.
                


### -field out


                    When <a href="https://msdn.microsoft.com/6e5f352b-5422-4bba-9525-7850bdddf0a5">WsMatchPolicyAlternative</a> returns NOERROR, the
                    entire contents of this structure will be filled out.
                


### -field out.channelProperty

 



