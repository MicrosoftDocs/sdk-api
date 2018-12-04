---
UID: NF:atscpsipparser.ISCTE_EAS.GetLocationCodes
title: ISCTE_EAS::GetLocationCodes
author: windows-sdk-content
description: The GetLocationCodes method returns location codes from the EAS table.
old-location: mstv\iscte_eas_getlocationcodes.htm
tech.root: mstv
ms.assetid: 31fa68d4-1719-4a93-bec9-6a7ba4f36c0b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetLocationCodes, GetLocationCodes method [Microsoft TV Technologies], GetLocationCodes method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetLocationCodes method, ISCTE_EAS.GetLocationCodes, ISCTE_EAS::GetLocationCodes, ISCTE_EASGetLocationCodes, atscpsipparser/ISCTE_EAS::GetLocationCodes, mstv.iscte_eas_getlocationcodes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - atscpsipparser.h
api_name:
 - ISCTE_EAS.GetLocationCodes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISCTE_EAS::GetLocationCodes


## -description


The <b>GetLocationCodes</b> method returns location codes from the EAS table.


## -parameters




### -param bIndex [in]

The zero-based index of the location codes to retrieve. Call <a href="https://msdn.microsoft.com/f498ead0-246d-4741-a995-45a5cf63847e">ISCTE_EAS::GetLocationCount</a> to get the number of locations.
          


### -param pbState [out]

Receives the state_code field.
          


### -param pbCountySubdivision [out]

Receives the county_subdivision field.
          


### -param pwCounty [out]

Receives the county_code field.
          


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_UNINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/f40e89f4-6a33-44a9-933c-bf38978f1cb2">ISCTE_EAS::Initialize</a> method was not called.

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




<a href="https://msdn.microsoft.com/7b5620c3-f460-4118-a8a2-9b2561bd12cf">ISCTE_EAS Interface</a>
 

 

