---
UID: NN:atscpsipparser.IATSC_STT
title: IATSC_STT
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_stt.htm
old-project: mstv
ms.assetid: 03e903e0-e722-42c6-b6b7-448fecc379b9
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IATSC_STT, IATSC_STT interface [Microsoft TV Technologies], IATSC_STT interface [Microsoft TV Technologies],described, IATSC_STTInterface, atscpsipparser/IATSC_STT, mstv.iatsc_stt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	IATSC_STT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_STT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IATSC_STT</b> interface enables the client to get data from a system time table (STT), which defines the current data and time of day. The <a href="https://msdn.microsoft.com/8aa6476c-9c75-4139-b5bc-6109ff223d98">IAtscPsipParser::GetSTT</a> method returns a pointer to this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSC_STT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IATSC_STT</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/527e64b4-c280-46d6-8579-a5755d4b242c">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors in the STT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c605ef2-a928-4c78-a2e4-c70142db66ac">GetDaylightSavings</a>
</td>
<td align="left" width="63%">
Returns the Daylight Savings Time Control bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/124c864a-a504-4f3c-836f-bdbe730beda7">GetGpsUtcOffset</a>
</td>
<td align="left" width="63%">
Returns the offset between GPS time and UTC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c735400d-9227-4f13-9703-ddafdf5772b0">GetProtocolVersion</a>
</td>
<td align="left" width="63%">
Returns the protocol version of the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4add19d8-9626-468f-8b15-993fb51f3c13">GetSystemTime</a>
</td>
<td align="left" width="63%">
Returns the current system time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f48ad31-ec6b-4d82-ba74-9901281a1857">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for the STT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e520dd8d-95f7-4b29-817c-14e3c663fdfc">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the STT for a descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

