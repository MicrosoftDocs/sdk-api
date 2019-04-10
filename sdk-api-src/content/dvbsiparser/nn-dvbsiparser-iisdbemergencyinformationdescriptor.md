---
UID: NN:dvbsiparser.IIsdbEmergencyInformationDescriptor
title: IIsdbEmergencyInformationDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) emergency information descriptor.
old-location: mstv\iisdbemergencyinformationdescriptor.htm
tech.root: mstv
ms.assetid: 1d098415-1e64-4b49-aa48-654b0d0da5df
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIsdbEmergencyInformationDescriptor, IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies], IIsdbEmergencyInformationDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbEmergencyInformationDescriptor, mstv.iisdbemergencyinformationdescriptor
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbEmergencyInformationDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbEmergencyInformationDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) emergency information descriptor. The emergency information descriptor appears as part of the service information (SI) in the program map table (PMT) or network information table (NIT). It is transmitted when an emergency warning is broadcast and includes all information required for the warning signal.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbEmergencyInformationDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbEmergencyInformationDescriptor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7bf09adf-6a04-4c3a-8c66-aea4e96c6936">GetAreaCode</a>
</td>
<td align="left" width="63%">
Gets area codes from  an ISDB emergency information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d23f1cc0-c6b0-4054-80be-36d7675fdec7">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of area code records from an ISDB emergency information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22520f2f-8a7f-45f3-86b1-a747fb33d7dc">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of an ISDB emergency information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/298f0637-eea1-4247-a9ff-cbe1a82fb8f6">GetServiceId</a>
</td>
<td align="left" width="63%">
Gets  the identifier for a broadcasting event from an  ISDB emergency information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf0c8d51-4ec8-4dad-8ef3-f18339ed0c0c">GetSignalLevel</a>
</td>
<td align="left" width="63%">
Gets a flag that indicates the emergency alarm signal type from an ISDB emergency information descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13593be1-073c-41df-b389-f0920d192c92">GetStartEndFlag</a>
</td>
<td align="left" width="63%">
Gets a flag from an ISDB emergency information descriptor that indicates whether an emergency alarm signal has started or finished broadcasting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0751a09-0336-48d7-a5f0-1182354774a4">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB emergency information descriptor.

</td>
</tr>
</table> 

