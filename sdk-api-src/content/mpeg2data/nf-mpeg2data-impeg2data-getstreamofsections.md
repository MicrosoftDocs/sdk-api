---
UID: NF:mpeg2data.IMpeg2Data.GetStreamOfSections
title: IMpeg2Data::GetStreamOfSections
author: windows-sdk-content
description: GetStreamOfSections is no longer available for use as of Windows 7.
old-location: mstv\impeg2data_getstreamofsections.htm
old-project: mstv
ms.assetid: 896080ff-cdf0-40b1-ba4e-d94de527d86e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetStreamOfSections, GetStreamOfSections method [Microsoft TV Technologies], GetStreamOfSections method [Microsoft TV Technologies],IMpeg2Data interface, IMpeg2Data interface [Microsoft TV Technologies],GetStreamOfSections method, IMpeg2Data.GetStreamOfSections, IMpeg2Data::GetStreamOfSections, IMpeg2DataGetStreamOfSections, mpeg2data/IMpeg2Data::GetStreamOfSections, mstv.impeg2data_getstreamofsections
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mpeg2data.h
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
tech.root: 
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mpeg2data.h
api_name:
-	IMpeg2Data.GetStreamOfSections
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMpeg2Data::GetStreamOfSections


## -description


<p class="CCE_Message">[<b>GetStreamOfSections</b> is no longer available for use as of Windows 7. Instead, use the <a href="https://msdn.microsoft.com/6f07b4d2-7a52-448c-9e9f-729bd5261757">IPSITables</a> interface to get program specific information (PSI) tables from an MPEG-2 transport stream.]

The <b>GetStreamOfSections</b> method starts an ongoing request for specific MPEG-2 table sections.


## -parameters




### -param pid [in]

Specifies the packet identifier (PID) of the transport stream packets to examine.


### -param tid [in]

Specifies the table identifier (TID) of the section to retrieve.


### -param pFilter [in]

Optional pointer to an <a href="https://msdn.microsoft.com/a7e66de7-d67b-4814-9849-076c3dd5afb1">MPEG2_FILTER</a> structure. The caller can use this parameter to exclude packets based on additional MPEG-2 header fields. This parameter can be <b>NULL</b>.


### -param hDataReadyEvent [in]

Handle to an event created by the caller. The filter signals this event whenever it receives new data.


### -param ppMpegStream [out]

Pointer to a variable that receives an <a href="https://msdn.microsoft.com/189c921a-ec49-48dc-8c60-3d3ec2a648ca">IMpeg2Stream</a> interface pointer. The caller must release the interface. Use this interface to retrieve the data when it arrives.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data Interface</a>
 

 

