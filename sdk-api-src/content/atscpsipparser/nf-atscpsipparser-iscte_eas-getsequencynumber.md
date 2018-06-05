---
UID: NF:atscpsipparser.ISCTE_EAS.GetSequencyNumber
title: ISCTE_EAS::GetSequencyNumber
author: windows-sdk-content
description: The GetSequencyNumbermethod returns the sequence number.
old-location: mstv\iscte_eas_getsequencynumber.htm
old-project: mstv
ms.assetid: c7988bb1-0c89-4f6f-beda-cbfd04a9b128
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetSequencyNumber, GetSequencyNumber method [Microsoft TV Technologies], GetSequencyNumber method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetSequencyNumber method, ISCTE_EAS.GetSequencyNumber, ISCTE_EAS::GetSequencyNumber, ISCTE_EASGetSequencyNumber, atscpsipparser/ISCTE_EAS::GetSequencyNumber, mstv.iscte_eas_getsequencynumber
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
-	ISCTE_EAS.GetSequencyNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISCTE_EAS::GetSequencyNumber


## -description


The <b>GetSequencyNumber</b>method returns the sequence number.


## -parameters




### -param pbVal [out]


            Receives the sequence_number field.
          


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
 

 

