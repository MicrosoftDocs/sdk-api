---
UID: NN:dvbsiparser.IIsdbEmergencyInformationDescriptor
title: IIsdbEmergencyInformationDescriptor (dvbsiparser.h)
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) emergency information descriptor.
helpviewer_keywords: ["IIsdbEmergencyInformationDescriptor","IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies]","IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IIsdbEmergencyInformationDescriptor","mstv.iisdbemergencyinformationdescriptor"]
old-location: mstv\iisdbemergencyinformationdescriptor.htm
tech.root: mstv
ms.assetid: 1d098415-1e64-4b49-aa48-654b0d0da5df
ms.date: 12/05/2018
ms.keywords: IIsdbEmergencyInformationDescriptor, IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies], IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbEmergencyInformationDescriptor, mstv.iisdbemergencyinformationdescriptor
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IIsdbEmergencyInformationDescriptor
 - dvbsiparser/IIsdbEmergencyInformationDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbEmergencyInformationDescriptor
---

# IIsdbEmergencyInformationDescriptor interface


## -description

Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) emergency information descriptor. The emergency information descriptor appears as part of the service information (SI) in the program map table (PMT) or network information table (NIT). It is transmitted when an emergency warning is broadcast and includes all information required for the warning signal.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbEmergencyInformationDescriptor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbEmergencyInformationDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbEmergencyInformationDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbemergencyinformationdescriptor-getareacode">GetAreaCode</a>
</td>
<td align="left" width="63%">
Gets area codes from  an ISDB emergency information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbemergencyinformationdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of area code records from an ISDB emergency information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbemergencyinformationdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of an ISDB emergency information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbemergencyinformationdescriptor-getserviceid">GetServiceId</a>
</td>
<td align="left" width="63%">
Gets  the identifier for a broadcasting event from an  ISDB emergency information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbemergencyinformationdescriptor-getsignallevel">GetSignalLevel</a>
</td>
<td align="left" width="63%">
Gets a flag that indicates the emergency alarm signal type from an ISDB emergency information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbemergencyinformationdescriptor-getstartendflag">GetStartEndFlag</a>
</td>
<td align="left" width="63%">
Gets a flag from an ISDB emergency information descriptor that indicates whether an emergency alarm signal has started or finished broadcasting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbemergencyinformationdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB emergency information descriptor.

</td>
</tr>
</table>