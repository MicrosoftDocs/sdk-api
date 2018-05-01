---
UID: NF:atscpsipparser.ISCTE_EAS.GetDuration
title: ISCTE_EAS::GetDuration method
author: windows-driver-content
description: The GetDuration method returns the expected duration of the alert.
old-location: mstv\iscte_eas_getduration.htm
old-project: mstv
ms.assetid: de644588-6247-44d2-9d19-53272af8529b
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetDuration method [Microsoft TV Technologies], GetDuration method [Microsoft TV Technologies], ISCTE_EAS interface, GetDuration,ISCTE_EAS.GetDuration, ISCTE_EAS, ISCTE_EAS interface [Microsoft TV Technologies], GetDuration method, ISCTE_EAS::GetDuration, ISCTE_EASGetDuration, atscpsipparser/ISCTE_EAS::GetDuration, mstv.iscte_eas_getduration
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
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	ISCTE_EAS.GetDuration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISCTE_EAS::GetDuration method


## -description


The <b>GetDuration</b> method returns the expected duration of the alert.


## -parameters




### -param pwVal [out]


            Receives the event_duration field. The value of the field is the expected duration in minutes, most significant bit first.
          


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
 

 

