---
UID: NF:atscpsipparser.ISCTE_EAS.GetExceptionService
title: ISCTE_EAS::GetExceptionService method
author: windows-driver-content
description: The GetExceptionService method returns information about an exception service.
old-location: mstv\iscte_eas_getexceptionservice.htm
old-project: mstv
ms.assetid: b9431651-4f8f-40a0-abd8-b162e5ad09ae
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetExceptionService method [Microsoft TV Technologies], GetExceptionService method [Microsoft TV Technologies], ISCTE_EAS interface, GetExceptionService,ISCTE_EAS.GetExceptionService, ISCTE_EAS, ISCTE_EAS interface [Microsoft TV Technologies], GetExceptionService method, ISCTE_EAS::GetExceptionService, ISCTE_EASGetExceptionService, atscpsipparser/ISCTE_EAS::GetExceptionService, mstv.iscte_eas_getexceptionservice
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
-	ISCTE_EAS.GetExceptionService
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISCTE_EAS::GetExceptionService method


## -description


The <b>GetExceptionService</b> method returns information about an exception service.


## -parameters




### -param bIndex [in]


            Zero-based index of the exception service to retrieve. Call <a href="https://msdn.microsoft.com/da98cf2f-a302-41d0-8226-18d6bb89be82">ISCTE_EAS::GetExceptionCount</a> to get the number of exception services.
          


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
 

 

