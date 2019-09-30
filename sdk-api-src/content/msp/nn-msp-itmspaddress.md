---
UID: NN:msp.ITMSPAddress
title: ITMSPAddress (msp.h)
author: windows-sdk-content
description: The ITMSPAddress interface is implemented by the MSP and represents a media service provider to the TAPI DLL. It is not exposed to end-user or server applications. TAPI 3 will call CoCreateInstance on this interface to create the MSP object.
old-location: tapi3\itmspaddress.htm
tech.root: Tapi
ms.assetid: 246a0bcd-0dbb-4b77-a1cd-e6378eaff889
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITMSPAddress, ITMSPAddress interface [TAPI 2.2], ITMSPAddress interface [TAPI 2.2],described, _tapi3_itmspaddress, msp/ITMSPAddress, tapi3.itmspaddress
ms.topic: interface
f1_keywords: 
 - "msp/ITMSPAddress"
req.header: msp.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msp.h
api_name:
 - ITMSPAddress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITMSPAddress interface


## -description


The 
<b>ITMSPAddress</b> interface is implemented by the MSP and represents a media service provider to the TAPI DLL. It is not exposed to end-user or server applications. TAPI 3 will call <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> on this interface to create the MSP object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITMSPAddress</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITMSPAddress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITMSPAddress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall">CreateMSPCall</a>
</td>
<td align="left" width="63%">
Create an 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a> object representing a new TAPI call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msp/nf-msp-itmspaddress-getevent">GetEvent</a>
</td>
<td align="left" width="63%">
Gets event information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msp/nf-msp-itmspaddress-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Called when the MSP is loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msp/nf-msp-itmspaddress-receivetspdata">ReceiveTSPData</a>
</td>
<td align="left" width="63%">
Called when the TSP sends asynchronous data to the MSP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msp/nf-msp-itmspaddress-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">
Called when the MSP is unloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall">ShutdownMSPCall</a>
</td>
<td align="left" width="63%">
Called when the call is being disconnected.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itsubstreamcontrol">ITSubStreamControl</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
 

 

