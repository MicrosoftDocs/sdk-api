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

# IMpeg2Data::GetTable


## -description


<p class="CCE_Message">[<b>GetTable</b> is no longer available for use as of Windows 7. Instead, use the <a href="https://msdn.microsoft.com/6f07b4d2-7a52-448c-9e9f-729bd5261757">IPSITables</a> interface to get program specific information (PSI) tables from an MPEG-2 transport stream.]

Retrieves a complete MPEG-2 PSI table. This method blocks until the filter receives all of the sections that make up the requested table, or until the specified time out elapses.


## -parameters




### -param pid [in]

Specifies the packet identifier (PID) of the transport stream packets to examine.


### -param tid [in]

Specifies the table identifier (TID) of the section to retrieve.


### -param pFilter [in]

Optional pointer to an <a href="https://msdn.microsoft.com/a7e66de7-d67b-4814-9849-076c3dd5afb1">MPEG2_FILTER</a> structure. The caller can use this parameter to exclude packets based on additional MPEG-2 header fields. This parameter can be <b>NULL</b>.


### -param dwTimeout [in]

Specifies a time-out value, in milliseconds. If the filter does not receive a matching section within the time-out period, the method fails.


### -param ppSectionList [out]

Receives an <a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a> interface pointer. Use this interface to retrieve the section data. The caller must release the interface.


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
<dt><b>MPEG2_E_SECTION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The filter did not receive a matching table section.

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



You can use the <i>pFilter</i> parameter to specify the Table_ID_extension field or the version number field. Otherwise, the filter caches these values from the first section that matches the search criteria. It uses those values to match subsequent sections.




## -see-also




<a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data Interface</a>
 

 

