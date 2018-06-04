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

# _WS_ENDPOINT_POLICY_EXTENSION structure


## -description



                This structure is used to specify an endpoint policy extension.
            


## -struct-fields




### -field policyExtension


                    The base policy extension that this policy extension derives from.
                


### -field assertionName


                    Name of the assertion to be retrieved as an extension.
                


### -field assertionNs


                  Namespace of the assertion to be retrieved as an extension.
                


### -field out


                    When <a href="https://msdn.microsoft.com/6e5f352b-5422-4bba-9525-7850bdddf0a5">WsMatchPolicyAlternative</a> returns NOERROR, the
                    fields of this structure will be filled out as follows:
                


### -field out.assertionValue

When <a href="https://msdn.microsoft.com/6e5f352b-5422-4bba-9525-7850bdddf0a5">WsMatchPolicyAlternative</a> returns NOERROR and if the specified assertion is found in the policy alternative, <b>assertionValue</b> returns the read-only content. Returned buffer should not be modified or freed. If not found, it is set to NULL. 




## -remarks




              This extension can be used to specify a custom assertion or an assertion that is
              supported by this library so that the application can
              retrieve the original XML form of the assertion. If one of the supported assertions
              is specified as an extension, the corresponding constraint should not be specified.
              For example, if http://schemas.xmlsoap.org/ws/2005/07/securitypolicy:TransportBinding
              is specified as an endpoint extension, <a href="https://msdn.microsoft.com/1f547d95-0a9a-44c5-81db-b92880238b1d">WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT</a>
              cannot be specified as a constraint.
          


              The following assertions are not allowed as policy extension because they might affect constraint 
              matching result if the assertion is handled as assertion. 

<pre class="syntax" xml:space="preserve"><code>
&lt;wsa09p:UsingAddressing.../&gt;
&lt;wsa10p:UsingAddressing.../&gt;
&lt;binp:BinaryEncoding.../&gt;
&lt;mtomp:OptimizedMimeSerialization.../&gt;</code></pre>


