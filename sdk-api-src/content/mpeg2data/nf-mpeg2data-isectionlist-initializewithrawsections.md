---
UID: NF:mpeg2data.ISectionList.InitializeWithRawSections
title: ISectionList::InitializeWithRawSections
author: windows-sdk-content
description: The InitializeWithRawSections method initializes the object with raw section data. This method allows for custom processing of section data.
old-location: mstv\isectionlist_initializewithrawsections.htm
old-project: mstv
ms.assetid: 61f1e99b-c375-4aa3-a11b-7e24c35f71ca
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISectionList interface [Microsoft TV Technologies],InitializeWithRawSections method, ISectionList.InitializeWithRawSections, ISectionList::InitializeWithRawSections, ISectionListInitializeWithRawSections, InitializeWithRawSections, InitializeWithRawSections method [Microsoft TV Technologies], InitializeWithRawSections method [Microsoft TV Technologies],ISectionList interface, mpeg2data/ISectionList::InitializeWithRawSections, mstv.isectionlist_initializewithrawsections
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mpeg2data.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2data.h
api_name:
 - ISectionList.InitializeWithRawSections
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

