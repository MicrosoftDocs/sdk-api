---
UID: NF:atscpsipparser.ISCTE_EAS.GetExceptionService
title: ISCTE_EAS::GetExceptionService (atscpsipparser.h)
description: The GetExceptionService method returns information about an exception service.helpviewer_keywords: ["GetExceptionService","GetExceptionService method [Microsoft TV Technologies]","GetExceptionService method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetExceptionService method","ISCTE_EAS.GetExceptionService","ISCTE_EAS::GetExceptionService","ISCTE_EASGetExceptionService","atscpsipparser/ISCTE_EAS::GetExceptionService","mstv.iscte_eas_getexceptionservice"]
old-location: mstv\iscte_eas_getexceptionservice.htm
tech.root: mstv
ms.assetid: b9431651-4f8f-40a0-abd8-b162e5ad09ae
ms.date: 12/05/2018
ms.keywords: GetExceptionService, GetExceptionService method [Microsoft TV Technologies], GetExceptionService method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetExceptionService method, ISCTE_EAS.GetExceptionService, ISCTE_EAS::GetExceptionService, ISCTE_EASGetExceptionService, atscpsipparser/ISCTE_EAS::GetExceptionService, mstv.iscte_eas_getexceptionservice
f1_keywords:
- atscpsipparser/ISCTE_EAS.GetExceptionService
dev_langs:
- c++
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
- ISCTE_EAS.GetExceptionService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISCTE_EAS::GetExceptionService


## -description


The <b>GetExceptionService</b> method returns information about an exception service.


## -parameters




### -param bIndex [in]

Zero-based index of the exception service to retrieve. Call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getexceptioncount">ISCTE_EAS::GetExceptionCount</a> to get the number of exception services.
          


### -param pbIBRef [out]

Receives the in_band_reference flag.
          


### -param pwFirst [out]

If the in_band_reference flag is <b>TRUE</b>, receives the exception_major_channel_number field. Otherwise, receives the exception_OOB_source_ID field.
          


### -param pwSecond [out]

If the in_band_reference flag is <b>TRUE</b>, receives the exception_minor_channel_number field. Otherwise, the value is undefined and this parameter should be ignored.
          


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
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
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
 

 

