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

# ISectionList::InitializeWithRawSections


## -description



The <b>InitializeWithRawSections</b> method initializes the object with raw section data. This method allows for custom processing of section data.




## -parameters




### -param pmplSections [in]

Pointer to an <a href="https://msdn.microsoft.com/83131e71-3e06-4d42-9f71-f2da95400b63">MPEG_PACKET_LIST</a> structure that contains a list of MPEG-2 sections.


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
<dt><b>MPEG2_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The object has already been initialized.

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



Use this method as follows:

<ol>
<li>Get the section data by calling the <a href="https://msdn.microsoft.com/896080ff-cdf0-40b1-ba4e-d94de527d86e">IMpeg2Data::GetStreamOfSections</a> method.</li>
<li>Create a new <b>SectionList</b> object and call <b>InitializeWithRawSections</b> with the section data.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList Interface</a>
 

 

