---
UID: NF:atscpsipparser.ISCTE_EAS.GetCountOfTableDescriptors
title: ISCTE_EAS::GetCountOfTableDescriptors
author: windows-sdk-content
description: The GetCountOfTableDescriptors method returns the number of descriptors in the EAS table.
old-location: mstv\iscte_eas_getcountoftabledescriptors.htm
tech.root: mstv
ms.assetid: 1d6cae55-233f-49e0-8ced-9dd21b0aa32b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetCountOfTableDescriptors, GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetCountOfTableDescriptors method, ISCTE_EAS.GetCountOfTableDescriptors, ISCTE_EAS::GetCountOfTableDescriptors, ISCTE_EASGetCountOfTableDescriptors, atscpsipparser/ISCTE_EAS::GetCountOfTableDescriptors, mstv.iscte_eas_getcountoftabledescriptors
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
 - ISCTE_EAS.GetCountOfTableDescriptors
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
- ISCTE_EAS.GetCountOfTableDescriptors
: 
---

# ISCTE_EAS::GetCountOfTableDescriptors


## -description


The <b>GetCountOfTableDescriptors</b> method returns the number of descriptors in the EAS table.


## -parameters




### -param pdwVal [out]

Receives the number of descriptors.
          


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
 

 

