---
UID: NS:wsdbase._WSDUdpRetransmitParams
title: WSDUdpRetransmitParams (wsdbase.h)
description: Defines the parameters for repeating a message transmission.
helpviewer_keywords: ["PWSDUdpRetransmitParams","PWSDUdpRetransmitParams structure pointer","WSDUdpRetransmitParams","WSDUdpRetransmitParams structure","_WSDUdpRetransmitParams","ncd.wsdupdretransmitparams","wsdbase/PWSDUdpRetransmitParams","wsdbase/WSDUdpRetransmitParams"]
old-location: ncd\wsdupdretransmitparams.htm
tech.root: ncd
ms.assetid: 41bf73d8-0b20-4c38-b8b4-85c39eff0d91
ms.date: 12/05/2018
ms.keywords: PWSDUdpRetransmitParams, PWSDUdpRetransmitParams structure pointer, WSDUdpRetransmitParams, WSDUdpRetransmitParams structure, _WSDUdpRetransmitParams, ncd.wsdupdretransmitparams, wsdbase/PWSDUdpRetransmitParams, wsdbase/WSDUdpRetransmitParams
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSDUdpRetransmitParams
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSDUdpRetransmitParams
 - wsdbase/_WSDUdpRetransmitParams
 - WSDUdpRetransmitParams
 - wsdbase/WSDUdpRetransmitParams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsdbase.h
api_name:
 - WSDUdpRetransmitParams
---

# WSDUdpRetransmitParams structure


## -description

Defines the parameters for repeating a message transmission.

## -struct-fields

### -field ulSendDelay

Time to wait before sending the first transmission, in milliseconds. Specify zero for no delay. Cannot be INFINITE.

### -field ulRepeat

Maximum number of transmissions to send. Specify a value between 1 and 256, inclusively.

### -field ulRepeatMinDelay

Minimum value of the range used to generate the initial delay value, in milliseconds. This value must be less than or equal to <b>ulRepeatMaxDelay</b>, can be zero, but cannot be INFINITE. See Remarks.

### -field ulRepeatMaxDelay

Maximum value of the range used to generate the initial delay value, in milliseconds. This value be less than or equal to <b>ulRepeatUpperDelay</b>, can be zero, but cannot be INFINITE. See Remarks.

### -field ulRepeatUpperDelay

Maximum delay to wait before sending message, in milliseconds. This value be can be zero, but cannot be INFINITE.

## -remarks

If <b>ulRepeatMinDelay</b>, <b>ulRepeatMaxDelay</b>, and <b>ulRepeatUpperDelay</b> are all zero, there is no delay in retransmission of the message.

WSD sends the first transmission after waiting <b>ulSendDelay</b>. WSD uses the other members to determine when to repeat the transmission, if necessary. WSD repeats the transmission up to <b>ulRepeat</b> times with increasing delays between transmission. WSD uses the <b>ulRepeatMinDelay</b>, <b>ulRepeatMaxDelay</b>, and <b>ulRepeatUpperDelay</b> members to determine the delay. 

WSD generates a random delay value in the range <b>ulRepeatMinDelay</b> to <b>ulRepeatMaxDelay</b> and waits this amount of time before repeating the transmission. All subsequent repeat attempts then double the current delay value until <b>ulRepeatUpperDelay</b> is reached. For example, if the initial random delay value is 50 and the upper delay value is 250, the second attempt will wait 50 milliseconds, the third attempt will wait 100 milliseconds, the fourth attempt will wait 200 milliseconds, and the remaining attempts will wait 250 milliseconds.

For details on how WSD uses these values to send messages, see Appendix I of the <a href="https://schemas.xmlsoap.org/ws/2004/09/soap-over-udp/">SOAP-over-UDP</a> specification.

## -see-also

<a href="/windows/desktop/api/wsdbase/nf-wsdbase-iwsdudpmessageparameters-getretransmitparams">IWSDUdpMessageParameters::GetRetransmitParams</a>



<a href="/windows/desktop/api/wsdbase/nf-wsdbase-iwsdudpmessageparameters-setretransmitparams">IWSDUdpMessageParameters::SetRetransmitParams</a>