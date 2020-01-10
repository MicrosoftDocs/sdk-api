---
UID: NN:rdpencomapi.IRDPSRAPIPerfCounterLogger
title: IRDPSRAPIPerfCounterLogger (rdpencomapi.h)
description: Enables a client application to implement custom performance logging.
old-location: rdp\irdpsrapiperfcounterlogger.htm
tech.root: rdp
ms.assetid: EAAA22B1-5D8A-4ED8-813B-58671B0EF7AA
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIPerfCounterLogger, IRDPSRAPIPerfCounterLogger class [RDP], IRDPSRAPIPerfCounterLogger class [RDP],described, rdp.irdpsrapiperfcounterlogger, rdpencomapi/IRDPSRAPIPerfCounterLogger
f1_keywords:
- rdpencomapi/IRDPSRAPIPerfCounterLogger
dev_langs:
- c++
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- RdpEncom.dll
api_name:
- IRDPSRAPIPerfCounterLogger
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRDPSRAPIPerfCounterLogger interface


## -description


Enables a client application to implement custom performance logging.

Applications obtain access to this object using the <a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiperfcounterloggingmanager">IRDPSRAPIPerfCounterLoggingManager</a><b>::</b><a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiperfcounterloggingmanager-createlogger">CreateLogger</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIPerfCounterLogger</b> class inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRDPSRAPIPerfCounterLogger</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRDPSRAPIPerfCounterLogger</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiperfcounterlogger-logvalue">LogValue</a>
</td>
<td align="left" width="63%">
Logs a value.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/rdp/windows-desktop-sharing-interfaces">Windows Desktop Sharing Interfaces</a>
 

 

