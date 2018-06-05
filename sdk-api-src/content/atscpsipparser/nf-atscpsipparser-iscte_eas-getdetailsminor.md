---
UID: NF:atscpsipparser.ISCTE_EAS.GetDetailsMinor
title: ISCTE_EAS::GetDetailsMinor
author: windows-sdk-content
description: The GetDetailsMinor method returns the minor channel number for the details channel.
old-location: mstv\iscte_eas_getdetailsminor.htm
old-project: mstv
ms.assetid: 59d43d84-2120-4200-b1e7-4603c1693018
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetDetailsMinor, GetDetailsMinor method [Microsoft TV Technologies], GetDetailsMinor method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetDetailsMinor method, ISCTE_EAS.GetDetailsMinor, ISCTE_EAS::GetDetailsMinor, ISCTE_EASGetDetailsMinor, atscpsipparser/ISCTE_EAS::GetDetailsMinor, mstv.iscte_eas_getdetailsminor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	ISCTE_EAS.GetDetailsMinor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISCTE_EAS::GetDetailsMinor


## -description


The <b>GetDetailsMinor</b> method returns the minor channel number for the details channel.


## -parameters




### -param pwVal [out]


            Receives the details_minor_channel_number field.
          


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
 

 

