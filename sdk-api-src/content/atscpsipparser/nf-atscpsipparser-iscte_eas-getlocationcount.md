---
UID: NF:atscpsipparser.ISCTE_EAS.GetLocationCount
title: ISCTE_EAS::GetLocationCount
author: windows-sdk-content
description: The GetLocationCount method returns the number of locations in the EAS table.
old-location: mstv\iscte_eas_getlocationcount.htm
tech.root: mstv
ms.assetid: f498ead0-246d-4741-a995-45a5cf63847e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetLocationCount, GetLocationCount method [Microsoft TV Technologies], GetLocationCount method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetLocationCount method, ISCTE_EAS.GetLocationCount, ISCTE_EAS::GetLocationCount, ISCTE_EASGetLocationCount, atscpsipparser/ISCTE_EAS::GetLocationCount, mstv.iscte_eas_getlocationcount
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
 - ISCTE_EAS.GetLocationCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISCTE_EAS::GetLocationCount


## -description


The <b>GetLocationCount</b> method returns the number of locations in the EAS table.


## -parameters




### -param pbVal [out]

Receives the location_code_count field.
          


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
 

 

