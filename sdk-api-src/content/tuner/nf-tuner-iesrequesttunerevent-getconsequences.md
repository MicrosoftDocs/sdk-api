---
UID: NF:tuner.IESRequestTunerEvent.GetConsequences
title: IESRequestTunerEvent::GetConsequences
author: windows-sdk-content
description: Gets a code that indicates the consequences of a device request for exclusive access to a tuner and its Conditional Access Services (CAS).
old-location: mstv\iesrequesttunerevent_getconsequences.htm
old-project: mstv
ms.assetid: 39588da7-90e7-4544-b53c-0f0ddb6cd951
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetConsequences, GetConsequences method [Microsoft TV Technologies], GetConsequences method [Microsoft TV Technologies],IESRequestTunerEvent interface, IESRequestTunerEvent interface [Microsoft TV Technologies],GetConsequences method, IESRequestTunerEvent.GetConsequences, IESRequestTunerEvent::GetConsequences, mstv.iesrequesttunerevent_getconsequences, tuner/IESRequestTunerEvent::GetConsequences
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IESRequestTunerEvent.GetConsequences
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESRequestTunerEvent::GetConsequences


## -description



      Gets a code that indicates the consequences of a device request for exclusive access to a tuner and its Conditional Access Services (CAS).


## -parameters




### -param pbyConsequences [out, retval]

Gets a 1-byte code indicating the consequences.  The code can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0x00</b></dt>
</dl>
</td>
<td width="60%">
Unspecified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0x01</b></dt>
</dl>
</td>
<td width="60%">
Reboot required. The device that is requesting exclusive access must reboot itself after it relinquishes access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>[Other]</b></dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/da1183a3-6f31-402a-b103-448cf13705a9">IESRequestTunerEvent</a>
 

 

