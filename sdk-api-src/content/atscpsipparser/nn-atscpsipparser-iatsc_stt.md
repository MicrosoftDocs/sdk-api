---
UID: NN:atscpsipparser.IATSC_STT
title: IATSC_STT (atscpsipparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_stt.htm
tech.root: mstv
ms.assetid: 03e903e0-e722-42c6-b6b7-448fecc379b9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IATSC_STT, IATSC_STT interface [Microsoft TV Technologies], IATSC_STT interface [Microsoft TV Technologies],described, IATSC_STTInterface, atscpsipparser/IATSC_STT, mstv.iatsc_stt
ms.topic: interface
f1_keywords: 
 - "atscpsipparser/IATSC_STT"
dev_langs:
 - c++
req.header: atscpsipparser.h
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
 - atscpsipparser.h
api_name:
 - IATSC_STT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IATSC_STT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IATSC_STT</b> interface enables the client to get data from a system time table (STT), which defines the current data and time of day. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getstt">IAtscPsipParser::GetSTT</a> method returns a pointer to this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSC_STT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IATSC_STT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IATSC_STT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_stt-getcountoftabledescriptors">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors in the STT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_stt-getdaylightsavings">GetDaylightSavings</a>
</td>
<td align="left" width="63%">
Returns the Daylight Savings Time Control bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_stt-getgpsutcoffset">GetGpsUtcOffset</a>
</td>
<td align="left" width="63%">
Returns the offset between GPS time and UTC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_stt-getprotocolversion">GetProtocolVersion</a>
</td>
<td align="left" width="63%">
Returns the protocol version of the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_stt-getsystemtime">GetSystemTime</a>
</td>
<td align="left" width="63%">
Returns the current system time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/dd389477(v=vs.85)">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for the STT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_stt-gettabledescriptorbytag">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the STT for a descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_stt-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

