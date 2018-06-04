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

# _WSD_APP_SEQUENCE structure


## -description


Represents application sequence information relating to WS-Discovery messages.


## -struct-fields




### -field InstanceId

The instance identifier.


### -field SequenceId

The sequence identifier.


### -field MessageNumber

The message number.


## -remarks



The application sequencing header block allows a receiver to maintain the sequence messages that contain this header block though they may have been received out of order. This allows proper sequencing of <a href="https://msdn.microsoft.com/a7402e02-9bdc-49ec-ba93-8a32f55b9dd8">Hello</a> and <a href="https://msdn.microsoft.com/7b9abfcc-28ab-4f29-af69-6dc68e3f51b6">Bye</a> messages from a target service.

The normative outline for the application sequence header block is:



<pre class="syntax" xml:space="preserve"><code>&lt;s:Envelope ...&gt; 
  &lt;s:Header ...&gt; 
    &lt;d:AppSequence InstanceId='xs:nonNegativeInteger' [SequenceId='xs:anyURI']? MessageNumber='xs:nonNegativeInteger' ... /&gt;
  &lt;/s:Header&gt; 
  &lt;s:Body ...&gt; ... 
  &lt;/s:Body&gt; 
&lt;/s:Envelope&gt;</code></pre>
The following describes normative constraints of this outline. 



<code>/s:Envelope/s:Header/d:AppSequence/@InstanceId</code>

This setting must be incremented by a value of at least 1 each time the service has terminated, lost state, and been restored. An application can set this value by using a counter that is incremented each time a service is restarted. The restart time of the service is expressed as seconds elapsed since 12:00 a.m. January 1, 1970.

<code>/s:Envelope/s:Header/d:AppSequence/@SequenceId</code>

 

This setting identifies a sequence within the context of an instance identifier. If it is omitted, the implied value is the null sequence. The value in this setting must be unique within ./@InstanceId.

<code>/s:Envelope/s:Header/d:AppSequence/@MessageNumber</code>

This setting identifies a message within the context of a sequence identifier and an instance identifier. must be incremented by a value of at least 1 for each message sent. Retransmission of this message at the transport level must maintain this value.




## -see-also




<a href="https://msdn.microsoft.com/f54eaa09-7ce8-4948-a0c5-edf2d054f6d5">AppSequence Validation Rules</a>
 

 

