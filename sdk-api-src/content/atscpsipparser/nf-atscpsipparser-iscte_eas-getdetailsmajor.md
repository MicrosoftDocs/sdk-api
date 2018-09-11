---
UID: NF:atscpsipparser.ISCTE_EAS.GetDetailsMajor
title: ISCTE_EAS::GetDetailsMajor
author: windows-sdk-content
description: The GetDetailsMajor method returns the major channel number for the details channel.
old-location: mstv\iscte_eas_getdetailsmajor.htm
tech.root: mstv
ms.assetid: ecb6f06d-ccf5-44f3-ba36-b24176c3a20e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetDetailsMajor, GetDetailsMajor method [Microsoft TV Technologies], GetDetailsMajor method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetDetailsMajor method, ISCTE_EAS.GetDetailsMajor, ISCTE_EAS::GetDetailsMajor, ISCTE_EASGetDetailsMajor, atscpsipparser/ISCTE_EAS::GetDetailsMajor, mstv.iscte_eas_getdetailsmajor
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
 - ISCTE_EAS.GetDetailsMajor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISCTE_EAS::GetDetailsMajor


## -description


The <b>GetDetailsMajor</b> method returns the major channel number for the details channel.


## -parameters




### -param pwVal [out]

Receives the details_major_channel_number field.
          


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
 

 

