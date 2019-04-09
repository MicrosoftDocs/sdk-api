---
UID: NF:atscpsipparser.ISCTE_EAS.GetDetailsOOBSourceID
title: ISCTE_EAS::GetDetailsOOBSourceID (atscpsipparser.h)
author: windows-sdk-content
description: The GetDetailsOOBSourceID method returns the source identifier of the virtual details channel for the emergency alert.
old-location: mstv\iscte_eas_getdetailsoobsourceid.htm
tech.root: mstv
ms.assetid: 50bf2acd-87e1-4b64-bf98-997603d56a0a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDetailsOOBSourceID, GetDetailsOOBSourceID method [Microsoft TV Technologies], GetDetailsOOBSourceID method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetDetailsOOBSourceID method, ISCTE_EAS.GetDetailsOOBSourceID, ISCTE_EAS::GetDetailsOOBSourceID, ISCTE_EASGetDetailsOOBSourceID, atscpsipparser/ISCTE_EAS::GetDetailsOOBSourceID, mstv.iscte_eas_getdetailsoobsourceid
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
 - ISCTE_EAS.GetDetailsOOBSourceID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISCTE_EAS::GetDetailsOOBSourceID


## -description


The <b>GetDetailsOOBSourceID</b> method returns the source identifier of the virtual details channel for the emergency alert.


## -parameters




### -param pwVal [out]

Receives the details_OOB_source_ID field.
          


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
 

 

