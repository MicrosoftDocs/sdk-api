---
UID: NF:atscpsipparser.ISCTE_EAS.GetEASEventCode
title: ISCTE_EAS::GetEASEventCode
author: windows-sdk-content
description: The GetEASEventCode method returns the EAS event code.
old-location: mstv\iscte_eas_geteaseventcode.htm
old-project: mstv
ms.assetid: 9618fb6f-61f3-44cf-9605-b47a6a1e9be6
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetEASEventCode, GetEASEventCode method [Microsoft TV Technologies], GetEASEventCode method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetEASEventCode method, ISCTE_EAS.GetEASEventCode, ISCTE_EAS::GetEASEventCode, ISCTE_EASGetEASEventCode, atscpsipparser/ISCTE_EAS::GetEASEventCode, mstv.iscte_eas_geteaseventcode
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - ISCTE_EAS.GetEASEventCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISCTE_EAS::GetEASEventCode


## -description


The <b>GetEASEventCode</b> method returns the EAS event code.


## -parameters




### -param pbVal [out]


            A pointer to a buffer that receives the EAS_event_code field. The caller must allocate the buffer, which must be large enough to hold the event code. To get the required size of the buffer, call <a href="https://msdn.microsoft.com/d6e05cd0-d043-4f15-b25b-28402035943b">ISCTE_EAS::GetEASEventCodeLen</a>. The event code consists of ASCII characters.
          


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




<a href="https://msdn.microsoft.com/d6e05cd0-d043-4f15-b25b-28402035943b">GetEASEventCodeLen</a>



<a href="https://msdn.microsoft.com/7b5620c3-f460-4118-a8a2-9b2561bd12cf">ISCTE_EAS Interface</a>
 

 

