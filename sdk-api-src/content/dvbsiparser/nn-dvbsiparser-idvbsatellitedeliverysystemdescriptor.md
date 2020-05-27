---
UID: NN:dvbsiparser.IDvbSatelliteDeliverySystemDescriptor
title: IDvbSatelliteDeliverySystemDescriptor (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDvbSatelliteDeliverySystemDescriptor","IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies]","IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies]","described","IDvbSatelliteDeliverySystemDescriptorInterface","dvbsiparser/IDvbSatelliteDeliverySystemDescriptor","mstv.idvbsatellitedeliverysystemdescriptor"]
old-location: mstv\idvbsatellitedeliverysystemdescriptor.htm
tech.root: mstv
ms.assetid: 814becf0-c98a-4419-aca6-d9b22d273e97
ms.date: 12/05/2018
ms.keywords: IDvbSatelliteDeliverySystemDescriptor, IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies], IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies],described, IDvbSatelliteDeliverySystemDescriptorInterface, dvbsiparser/IDvbSatelliteDeliverySystemDescriptor, mstv.idvbsatellitedeliverysystemdescriptor
f1_keywords:
- dvbsiparser/IDvbSatelliteDeliverySystemDescriptor
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: 
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
- dvbsiparser.h
api_name:
- IDvbSatelliteDeliverySystemDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbSatelliteDeliverySystemDescriptor interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDvbSatelliteDeliverySystemDescriptor</b> interface enables the client to get a satellite delivery system descriptor from a DVB stream. The satellite delivery system descriptor may be present in the network information table (NIT). For more information, refer to ETSI EN 300 468.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbSatelliteDeliverySystemDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbSatelliteDeliverySystemDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbSatelliteDeliverySystemDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsatellitedeliverysystemdescriptor-getfecinner">GetFECInner</a>
</td>
<td align="left" width="63%">
Returns the inner forward error correction (FEC) scheme.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsatellitedeliverysystemdescriptor-getfrequency">GetFrequency</a>
</td>
<td align="left" width="63%">
Returns the frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsatellitedeliverysystemdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Returns the length of the descriptor body.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsatellitedeliverysystemdescriptor-getmodulation">GetModulation</a>
</td>
<td align="left" width="63%">
Returns the modulation scheme.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsatellitedeliverysystemdescriptor-getorbitalposition">GetOrbitalPosition</a>
</td>
<td align="left" width="63%">
Returns the orbital position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsatellitedeliverysystemdescriptor-getpolarization">GetPolarization</a>
</td>
<td align="left" width="63%">
Returns the polarization of the transmitted signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsatellitedeliverysystemdescriptor-getsymbolrate">GetSymbolRate</a>
</td>
<td align="left" width="63%">
Returns the symbol rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsatellitedeliverysystemdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Returns the descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsatellitedeliverysystemdescriptor-getwesteastflag">GetWestEastFlag</a>
</td>
<td align="left" width="63%">
Returns a flag that specifies whether the satellite is in the western or eastern part of the orbit.

</td>
</tr>
</table> 


## -remarks



To obtain a pointer to this interface, do the following:

<ol>
<li>Call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getnit">IDvbSiParser::GetNIT</a> to get the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_nit">IDVB_NIT</a> interface.</li>
<li>Call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_nit-getrecorddescriptorbytag">IDVB_NIT::GetRecordDescriptorByTag</a> and pass in the satellite delivery system descriptor tag (0x43). If the descriptor is present, the method returns an <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> pointer.</li>
<li>Query the returned <b>IGenericDescriptor</b> pointer for the <b>IDvbSatelliteDeliverySystemDescriptor</b> interface.</li>
</ol>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

