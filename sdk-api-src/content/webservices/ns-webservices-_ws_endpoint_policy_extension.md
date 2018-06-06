---
UID: NS:webservices._WS_ENDPOINT_POLICY_EXTENSION
title: "_WS_ENDPOINT_POLICY_EXTENSION"
author: windows-sdk-content
description: This structure is used to specify an endpoint policy extension.
old-location: wsw\ws_endpoint_policy_extension.htm
old-project: wsw
ms.assetid: 8bcb2466-fb07-4a15-82a2-87fc7f0f3d92
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_ENDPOINT_POLICY_EXTENSION, WS_ENDPOINT_POLICY_EXTENSION structure [Web Services for Windows], _WS_ENDPOINT_POLICY_EXTENSION, webservices/WS_ENDPOINT_POLICY_EXTENSION, wsw.ws_endpoint_policy_extension
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WS_ENDPOINT_POLICY_EXTENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_ENDPOINT_POLICY_EXTENSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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


