---
UID: NS:wsdtypes._WSD_APP_SEQUENCE
title: WSD_APP_SEQUENCE (wsdtypes.h)
description: Represents application sequence information relating to WS-Discovery messages.
helpviewer_keywords: ["WSD_APP_SEQUENCE","WSD_APP_SEQUENCE structure","ncd.wsd_app_sequence_struct","wsdtypes/WSD_APP_SEQUENCE"]
old-location: ncd\wsd_app_sequence_struct.htm
tech.root: ncd
ms.assetid: e9aa8e2f-0162-4f2e-ad70-54b6352105f9
ms.date: 12/05/2018
ms.keywords: WSD_APP_SEQUENCE, WSD_APP_SEQUENCE structure, ncd.wsd_app_sequence_struct, wsdtypes/WSD_APP_SEQUENCE
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: WSD_APP_SEQUENCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_APP_SEQUENCE
 - wsdtypes/_WSD_APP_SEQUENCE
 - WSD_APP_SEQUENCE
 - wsdtypes/WSD_APP_SEQUENCE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_APP_SEQUENCE
---

# WSD_APP_SEQUENCE structure


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

The application sequencing header block allows a receiver to maintain the sequence messages that contain this header block though they may have been received out of order. This allows proper sequencing of <a href="/windows/desktop/WsdApi/hello-message">Hello</a> and <a href="/windows/desktop/WsdApi/bye-message">Bye</a> messages from a target service.

The normative outline for the application sequence header block is:

``` syntax
<s:Envelope ...>
  <s:Header ...>
    <d:AppSequence InstanceId='xs:nonNegativeInteger' [SequenceId='xs:anyURI']? MessageNumber='xs:nonNegativeInteger' ... />
  </s:Header>
  <s:Body ...> ...
  </s:Body>
</s:Envelope>
```

The following describes normative constraints of this outline. 



<code>/s:Envelope/s:Header/d:AppSequence/@InstanceId</code>

This setting must be incremented by a value of at least 1 each time the service has terminated, lost state, and been restored. An application can set this value by using a counter that is incremented each time a service is restarted. The restart time of the service is expressed as seconds elapsed since 12:00 a.m. January 1, 1970.

<code>/s:Envelope/s:Header/d:AppSequence/@SequenceId</code>

 

This setting identifies a sequence within the context of an instance identifier. If it is omitted, the implied value is the null sequence. The value in this setting must be unique within ./@InstanceId.

<code>/s:Envelope/s:Header/d:AppSequence/@MessageNumber</code>

This setting identifies a message within the context of a sequence identifier and an instance identifier. must be incremented by a value of at least 1 for each message sent. Retransmission of this message at the transport level must maintain this value.

## -see-also

<a href="/windows/desktop/WsdApi/appsequence-validation-rules">AppSequence Validation Rules</a>
