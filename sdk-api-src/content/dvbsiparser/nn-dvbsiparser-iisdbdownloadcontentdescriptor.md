---
UID: NN:dvbsiparser.IIsdbDownloadContentDescriptor
title: IIsdbDownloadContentDescriptor
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) download content descriptor.
old-location: mstv\iisdbdownloadcontentdescriptor.htm
tech.root: MSTV
ms.assetid: beef626c-64b1-4f49-bb21-69022907004d
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IIsdbDownloadContentDescriptor, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies], IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbDownloadContentDescriptor, mstv.iisdbdownloadcontentdescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IIsdbDownloadContentDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbDownloadContentDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The download content descriptor appears in the ISDB Service Information as part of the software download trigger table (SDTT) and provides details about content and scheduling related to downloading.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbDownloadContentDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbDownloadContentDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbDownloadContentDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/054fe987-49e1-4434-a9b9-6b1030fa2c41">GetCompatiblityDescriptor</a>
</td>
<td align="left" width="63%">
Gets data from the compatibility descriptor in an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8fc770c-aa37-4f97-beb5-6e5747904a6c">GetCompatiblityDescriptorLength</a>
</td>
<td align="left" width="63%">
Gets the length of the compatibility descriptor  from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07edb403-6674-4673-928c-91e7df9fe9da">GetComponentSize</a>
</td>
<td align="left" width="63%">
 Gets the total size of components within an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4ba2fbd-4349-48e3-81dd-622442409060">GetComponentTag</a>
</td>
<td align="left" width="63%">
 Gets a tag that identifies the downloaded stream from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5a0b8e1-bb88-4ef6-ab25-b35b3d39fef0">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of records in an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b57eba56-b9d6-4555-8d5d-80fd2b9fd23f">GetDownloadId</a>
</td>
<td align="left" width="63%">
 Gets the download identifier from an ISDB download content descriptor

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df104d6d-1436-4c7d-b250-b740e1f70c07">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the values of flags  from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e85f026-66bf-4c13-b476-3aca9e28b3b6">GetLeakRate</a>
</td>
<td align="left" width="63%">
 Gets the leak rate of the transport buffer from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0eb0e44-da1c-4b52-9c96-199db6d3288e">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c714b2f2-e787-40cc-b57b-d56b54dc8966">GetRecordModuleId</a>
</td>
<td align="left" width="63%">
 Gets the identifier for a carousel module from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f9dc48c-7df3-498b-b9ff-4610bd9e7ac2">GetRecordModuleInfo</a>
</td>
<td align="left" width="63%">
Gets the module descriptor field from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/963f44be-e0f4-4cb7-8e71-8641af0cd700">GetRecordModuleInfoLength</a>
</td>
<td align="left" width="63%">
 Gets the length of the module_info_byte field that contains descriptors for the module from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/395264ee-63de-4de4-bd28-4d5c4634dcf3">GetRecordModuleSize</a>
</td>
<td align="left" width="63%">
 Gets the size of a carousel module from an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a78c3f3b-aaa2-4b5e-9cf8-7746f20fafc2">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/023e2b6f-0f38-4550-a839-29c254970219">GetTextLanguageCode</a>
</td>
<td align="left" width="63%">
 Gets the three-character ISO 639 language code used for the service description in an ISDB download content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf26ff9b-02d8-4470-bde5-6a18c62c6511">GetTextW</a>
</td>
<td align="left" width="63%">
 Gets the service description from an ISDB download content descriptor, in Unicode string format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec1bd153-e637-4046-8d7b-f2868c4909dd">GetTimeOutValueDII</a>
</td>
<td align="left" width="63%">
 Gets the recommended download timeout interval from an ISDB download content descriptor.

</td>
</tr>
</table> 

