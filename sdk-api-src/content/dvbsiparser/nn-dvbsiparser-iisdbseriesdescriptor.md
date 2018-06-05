---
UID: NN:dvbsiparser.IIsdbSeriesDescriptor
title: IIsdbSeriesDescriptor
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) series descriptor.
old-location: mstv\iisdbseriesdescriptor.htm
old-project: mstv
ms.assetid: 07c4debc-1817-46ac-9f67-9b8637a04662
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IIsdbSeriesDescriptor, IIsdbSeriesDescriptor interface [Microsoft TV Technologies], IIsdbSeriesDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbSeriesDescriptor, mstv.iisdbseriesdescriptor
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbSeriesDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbSeriesDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) series descriptor. The series descriptor appears in the ISDB Service Information as part of the event information table (EIT) and defines series information among multiple events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbSeriesDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbSeriesDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbSeriesDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a28ff17-4a5e-4245-845e-1307830fb3fd">GetEpisodeNumber</a>
</td>
<td align="left" width="63%">
 Gets the episode number of a series from an ISDB series descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d658904-4f81-443b-b69d-814e606dabc4">GetExpireDate</a>
</td>
<td align="left" width="63%">
Gets a date that identifies the end date of a series from  an ISDB series descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23cae82f-a40f-47c6-b9ee-0d91a87d9b70">GetLastEpisodeNumber</a>
</td>
<td align="left" width="63%">
 Gets the number of the final episode of a series from an ISDB series descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/703e4406-7fca-4d96-83de-56fd2ff52d30">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of  an ISDB series descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba37c512-bbde-42ad-80fe-9d67f48299b6">GetProgramPattern</a>
</td>
<td align="left" width="63%">
 Gets a code that identifies the how often a series is broadcast from an ISDB series descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04b47836-0c27-41da-b71d-6c4abca6dd56">GetRepeatLabel</a>
</td>
<td align="left" width="63%">
 Gets the label that identifies repeat broadcasts of a series from ISDB series descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90de5108-1d40-475b-83fe-20b68fa3f748">GetSeriesId</a>
</td>
<td align="left" width="63%">
 Gets the series identifier from an ISDB series descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7638dc5b-6542-42f4-9996-f851704098a0">GetSeriesNameW</a>
</td>
<td align="left" width="63%">
 Gets the name of the series from an ISDB series descriptor, in Unicode string format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f67fcf4-76b6-4e1c-99a1-e09b406b5bd9">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB series descriptor.

</td>
</tr>
</table> 

