---
UID: NF:atscpsipparser.ISCTE_EAS.GetAlertPriority
title: ISCTE_EAS::GetAlertPriority
author: windows-sdk-content
description: The GetAlertPriority method returns the alert priority.
old-location: mstv\iscte_eas_getalertpriority.htm
tech.root: mstv
ms.assetid: 3862ae19-972b-4822-8b52-5a868a2fc58d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetAlertPriority, GetAlertPriority method [Microsoft TV Technologies], GetAlertPriority method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetAlertPriority method, ISCTE_EAS.GetAlertPriority, ISCTE_EAS::GetAlertPriority, ISCTE_EASGetAlertPriority, atscpsipparser/ISCTE_EAS::GetAlertPriority, mstv.iscte_eas_getalertpriority
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
 - ISCTE_EAS.GetAlertPriority
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- atscpsipparser.h
: 
- ISCTE_EAS.GetAlertPriority
: 
---

# ISCTE_EAS::GetAlertPriority


## -description


The <b>GetAlertPriority</b> method returns the alert priority.


## -parameters




### -param pbVal [out]

Receives the alert_priority field.
          


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
 

 

