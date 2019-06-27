---
UID: NF:atscpsipparser.ISCTE_EAS.GetTimeRemaining
title: ISCTE_EAS::GetTimeRemaining (atscpsipparser.h)
author: windows-sdk-content
description: The GetTimeRemaining method returns the time that remains in the alert message.
old-location: mstv\iscte_eas_gettimeremaining.htm
tech.root: mstv
ms.assetid: 4d04408f-a1ff-41cf-8ab0-1f30e700b07b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTimeRemaining, GetTimeRemaining method [Microsoft TV Technologies], GetTimeRemaining method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetTimeRemaining method, ISCTE_EAS.GetTimeRemaining, ISCTE_EAS::GetTimeRemaining, ISCTE_EASGetTimeRemaining, atscpsipparser/ISCTE_EAS::GetTimeRemaining, mstv.iscte_eas_gettimeremaining
ms.topic: method
f1_keywords: 
 - "atscpsipparser/ISCTE_EAS.GetTimeRemaining"
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
 - ISCTE_EAS.GetTimeRemaining
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISCTE_EAS::GetTimeRemaining


## -description


The <b>GetTimeRemaining</b> method returns the time that remains in the alert message.


## -parameters




### -param pbVal [out]

Receives the alert_message_time_remaining field.
          


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
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-initialize">ISCTE_EAS::Initialize</a> method was not called.

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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iscte_eas">ISCTE_EAS Interface</a>
 

 

