---
UID: NS:webservices._WS_SECURITY_DESCRIPTION
title: "_WS_SECURITY_DESCRIPTION"
author: windows-sdk-content
description: The top-level structure used to specify the security requirements for a channel (on the client side) or a listener (on the server side).
old-location: wsw\ws_security_description.htm
tech.root: wsw
ms.assetid: b9490f00-877c-4d9f-b361-eaca343cdee0
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_SECURITY_DESCRIPTION, WS_SECURITY_DESCRIPTION structure [Web Services for Windows], _WS_SECURITY_DESCRIPTION, webservices/WS_SECURITY_DESCRIPTION, wsw.ws_security_description
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
 - WS_SECURITY_DESCRIPTION
product: Windows
targetos: Windows
req.typenames: WS_SECURITY_DESCRIPTION
req.redist: 
---

# _WS_SECURITY_DESCRIPTION structure


## -description


The top-level structure used to specify the security requirements for
a <a href="https://msdn.microsoft.com/4bef6f97-06f1-442a-8b84-869776f0541d">channel</a> (on the client side) or a <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">listener</a> (on the server side).

            


## -struct-fields




### -field securityBindings

The array of pointers to security bindings.  The set of security
bindings supplies determines the kind of security applied to the
channel.  Each security binding specifies one security token.
                


### -field securityBindingCount

The count of elements in the securityBindings array.
                


### -field properties

The array of properties specifying the optional channel-wide security
settings.  Each <a href="https://msdn.microsoft.com/676079cd-6ca8-486b-9604-172423210ad5">WS_SECURITY_PROPERTY</a> in the array is a key-value
pair and must use a key defined in <a href="https://msdn.microsoft.com/98a824c9-11dd-4433-ae8f-2e6b6f6a520f">WS_SECURITY_PROPERTY_ID</a>.  This field can be <b>NULL</b>,
and if it is <b>NULL</b>, the default value will be used for each security
channel setting.
                


### -field propertyCount

The count of elements in the properties array.
                


## -remarks



The figure below illustrates the structure of a security description.
            

<img alt="" src="./images/SecurityDescription.png"/>



