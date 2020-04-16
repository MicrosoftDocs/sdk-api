---
UID: NN:dvbsiparser.IIsdbSIParameterDescriptor
title: IIsdbSIParameterDescriptor (dvbsiparser.h)
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) service information (SI) parameter descriptor. The SI parameter descriptor appears in the program map table (PMT) or network information table (NIT).helpviewer_keywords: ["IIsdbSIParameterDescriptor","IIsdbSIParameterDescriptor interface [Microsoft TV Technologies]","IIsdbSIParameterDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IIsdbSIParameterDescriptor","mstv.iisdbsiparameterdescriptor"]
old-location: mstv\iisdbsiparameterdescriptor.htm
tech.root: mstv
ms.assetid: 264ae78d-cd72-49ff-b99b-2af637cc2917
ms.date: 12/05/2018
ms.keywords: IIsdbSIParameterDescriptor, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies], IIsdbSIParameterDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbSIParameterDescriptor, mstv.iisdbsiparameterdescriptor
f1_keywords:
- dvbsiparser/IIsdbSIParameterDescriptor
dev_langs:
- c++
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
- IIsdbSIParameterDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbSIParameterDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) service information (SI) parameter descriptor. The SI parameter descriptor appears in the program map table (PMT) or network information table (NIT).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbSIParameterDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbSIParameterDescriptor</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparameterdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of  an ISDB SI parameter descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparameterdescriptor-getparameterversion">GetParameterVersion</a>
</td>
<td align="left" width="63%">
Gets the version number of a parameter from an ISDB SI parameter descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparameterdescriptor-getrecordnumberoftable">GetRecordNumberOfTable</a>
</td>
<td align="left" width="63%">
Gets the number of table descriptors in an ISDB SI parameter descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparameterdescriptor-gettabledescriptionbytes">GetTableDescriptionBytes</a>
</td>
<td align="left" width="63%">
Gets description data from a table descriptor in an ISDB SI parameter descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparameterdescriptor-gettabledescriptionlength">GetTableDescriptionLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a table descriptor in an ISDB SI parameter descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparameterdescriptor-gettableid">GetTableId</a>
</td>
<td align="left" width="63%">
Gets an identifier for a table descriptor in an ISDB SI parameter descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparameterdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
 Gets the tag that identifies an ISDB SI parameter descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparameterdescriptor-getupdatetime">GetUpdateTime</a>
</td>
<td align="left" width="63%">
Gets the time at which a parameter becomes valid from an ISDB SI parameter descriptor. 

</td>
</tr>
</table> 

