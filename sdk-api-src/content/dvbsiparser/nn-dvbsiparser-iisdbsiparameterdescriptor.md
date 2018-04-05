---
UID: NN:dvbsiparser.IIsdbSIParameterDescriptor
title: IIsdbSIParameterDescriptor
author: windows-driver-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) service information (SI) parameter descriptor. The SI parameter descriptor appears in the program map table (PMT) or network information table (NIT).
old-location: mstv\iisdbsiparameterdescriptor.htm
old-project: mstv
ms.assetid: 264ae78d-cd72-49ff-b99b-2af637cc2917
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IIsdbSIParameterDescriptor, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies], IIsdbSIParameterDescriptor interface [Microsoft TV Technologies], described, dvbsiparser/IIsdbSIParameterDescriptor, mstv.iisdbsiparameterdescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbSIParameterDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbSIParameterDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) service information (SI) parameter descriptor. The SI parameter descriptor appears in the program map table (PMT) or network information table (NIT).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbSIParameterDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbSIParameterDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbSIParameterDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e4ac80d-30a9-4879-9cd3-a3964c675b27">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of  an ISDB SI parameter descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ca9d5d3-d96f-4437-9d22-0166a3fbc593">GetParameterVersion</a>
</td>
<td align="left" width="63%">
Gets the version number of a parameter from an ISDB SI parameter descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12f7af61-494e-4597-8672-47ea9552be62">GetRecordNumberOfTable</a>
</td>
<td align="left" width="63%">
Gets the number of table descriptors in an ISDB SI parameter descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd73b221-b7b5-43c8-bbdf-f1ea559a0a4e">GetTableDescriptionBytes</a>
</td>
<td align="left" width="63%">
Gets description data from a table descriptor in an ISDB SI parameter descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3dc78381-ac39-4e88-bfe2-bfb91c993576">GetTableDescriptionLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a table descriptor in an ISDB SI parameter descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43b19e3d-20b0-4356-9c84-f47006635e2c">GetTableId</a>
</td>
<td align="left" width="63%">
Gets an identifier for a table descriptor in an ISDB SI parameter descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d38b158-39b0-4960-b392-086595680133">GetTag</a>
</td>
<td align="left" width="63%">
 Gets the tag that identifies an ISDB SI parameter descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cfe8387-4edf-453b-b41b-768496eae76c">GetUpdateTime</a>
</td>
<td align="left" width="63%">
Gets the time at which a parameter becomes valid from an ISDB SI parameter descriptor. 

</td>
</tr>
</table> 

