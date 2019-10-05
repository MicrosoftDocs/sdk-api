---
UID: NN:wsdbase.IWSDUdpMessageParameters
title: IWSDUdpMessageParameters (wsdbase.h)
author: windows-sdk-content
description: Use this interface to specify how often WSD repeats the message transmission.
old-location: ncd\iwsdudpmessageparameters.htm
tech.root: WsdApi
ms.assetid: 3af6e0ff-c0b9-47af-b018-37567f614adc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDUdpMessageParameters, IWSDUdpMessageParameters interface, IWSDUdpMessageParameters interface,described, ncd.iwsdudpmessageparameters, wsdbase/IWSDUdpMessageParameters
ms.topic: interface
f1_keywords: 
 - "wsdbase/IWSDUdpMessageParameters"
dev_langs:
 - c++
req.header: wsdbase.h
req.include-header: 
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
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDUdpMessageParameters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDUdpMessageParameters interface


## -description


Use this interface to specify how often WSD repeats the message transmission.

To get this interface from a UDP message sent during discovery, call the  <b>QueryInterface</b> method of <a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a> passing __uuidof(IWSDUdpMessageParameters) as the interface identifier.

You can also call <a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-wsdcreateudpmessageparameters">WSDCreateUdpMessageParameters</a> to retrieve this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDUdpMessageParameters</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a>. <b>IWSDUdpMessageParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDUdpMessageParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdudpmessageparameters-getretransmitparams">GetRetransmitParams</a>
</td>
<td align="left" width="63%">
Retrieves the values that WSD uses to determine how often to repeat the message transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdudpmessageparameters-setretransmitparams">SetRetransmitParams</a>
</td>
<td align="left" width="63%">
Sets the values that WSD uses to determine how often to repeat the message transmission.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a>
 

 

