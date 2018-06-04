---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDvbSiParser2::GetEIT2


## -description







The <b>GetEIT2</b> method gets the event information table (EIT). 


## -parameters




### -param tableId [in]


            Specifies the table identifier of the EIT. Use one of the following values.
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DVB_EIT_ACTUAL_TID"></a><a id="dvb_eit_actual_tid"></a><dl>
<dt><b>DVB_EIT_ACTUAL_TID</b></dt>
<dt> 0x4E</dt>
</dl>
</td>
<td width="60%">
Present/following EIT for this transport stream.

</td>
</tr>
<tr>
<td width="40%"><a id="DVB_EIT_OTHER_TID_"></a><a id="dvb_eit_other_tid_"></a><dl>
<dt><b>DVB_EIT_OTHER_TID </b></dt>
<dt>0x4F</dt>
</dl>
</td>
<td width="60%">
Present/following EIT for another transport stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x50 – 0x5F</dt>
</dl>
</td>
<td width="60%">
Schedule EIT for this transport stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x60 – 0x6F</dt>
</dl>
</td>
<td width="60%">
Schedule EIT for another transport stream.

</td>
</tr>
</table>
 


### -param pwServiceId [in]


            An optional parameter that contains a service identifier. You can use this value to filter the request. Otherwise, set this parameter to <b>NULL</b>.
          


### -param pbSegment [in]


            An optional parameter that contains a segment number. You can use this value to filter the request. Otherwise, set this parameter to <b>NULL</b>.
          


### -param ppEIT [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/9d93130c-12fb-4c76-98c1-cdfae113cf2c">IDVB_EIT2</a> interface. The caller must release the interface.
          


## -returns




            The method returns an <b>HRESULT</b>. Possible values include those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_SECTION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The filter did not receive the table in the allotted time.

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
 




## -remarks




        The method fails if the filter does not receive a matching table within a predetermined length of time.
      




## -see-also




<a href="https://msdn.microsoft.com/085808e7-b067-470e-9edd-8795f4881485">IDvbSiParser2</a>
 

 

