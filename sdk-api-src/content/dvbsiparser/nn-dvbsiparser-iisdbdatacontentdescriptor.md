---
UID: NN:dvbsiparser.IIsdbDataContentDescriptor
title: IIsdbDataContentDescriptor
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) data content descriptor.
old-location: mstv\iisdbdatacontentdescriptor.htm
tech.root: mstv
ms.assetid: 91d55991-5994-4104-9a8f-01cfc347a96f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IIsdbDatacontentDescriptor, IIsdbDatacontentDescriptor interface [Microsoft TV Technologies], IIsdbDatacontentDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbDatacontentDescriptor, mstv.iisdbdatacontentdescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Dvbsiparser.h
api_name:
 - IIsdbDatacontentDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbDataContentDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) data content descriptor. The data content descriptor appears in the ISDB Service Information as part of the event information table (EIT) and provides details about the content of a data broadcasting event.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbDatacontentDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbDatacontentDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbDatacontentDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4198ec3c-f2a3-4517-8efb-81dfb9f8c01d">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
 Gets the number of component records in  an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8a3e399-5004-41ee-a7eb-4c583a1fdd45">GetDataComponentId</a>
</td>
<td align="left" width="63%">
 Gets a component identifier from an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f8f9e55-cc03-4f07-918e-19199485c8d4">GetEntryComponent</a>
</td>
<td align="left" width="63%">
 Gets a code that indicates the first referenced component stream in the descriptor from an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbf89870-e258-43d8-8312-edc53998e51a">GetLanguageCode</a>
</td>
<td align="left" width="63%">
Gets the three-character ISO 639 language code from an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51546c62-5042-460d-a792-2253bd57df13">GetLength</a>
</td>
<td align="left" width="63%">
 Gets the body length of an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3668c323-6808-4bc4-b372-37647ef3fdd8">GetRecordComponentRef</a>
</td>
<td align="left" width="63%">
Gets a broadcaster-defined component tag that identifies a component stream from ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b02c315e-322d-478e-8be1-c833df49ed56">GetSelectorBytes</a>
</td>
<td align="left" width="63%">
 Gets data from the selector area of an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/485ac963-e85a-41cc-adcd-93590b327061">GetSelectorLength</a>
</td>
<td align="left" width="63%">
Gets the length of the selector area from an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/308f44d6-0aae-418e-8aad-cc812c0cdb8a">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB data content descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7abc2e2-4fb5-4b8b-8678-416056836aee">GetTextW</a>
</td>
<td align="left" width="63%">
 Gets the text that describes a component in an ISDB data content descriptor, in Unicode text format.

</td>
</tr>
</table> 

