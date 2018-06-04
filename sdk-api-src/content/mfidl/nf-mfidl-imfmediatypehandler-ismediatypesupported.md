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

# IMFMediaTypeHandler::IsMediaTypeSupported


## -description



Queries whether the object supports a specified media type.




## -parameters




### -param pMediaType [in]


            Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type to check.
          


### -param ppMediaType [out]


            Receives a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the closest matching media type, or receives the value <b>NULL</b>. If non-<b>NULL</b>, the caller must release the interface. This parameter can be <b>NULL</b>. See Remarks.
          


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">

                The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">

                The object does not support this media type.
              

</td>
</tr>
</table>
 




## -remarks




        If the object supports the media type given in <i>pMediaType</i>, the method returns <b>S_OK</b>. For a media source, it means the source can generate data that conforms to that media type. For a media sink, it means the sink can receive data that conforms to that media type. If the object does not support the media type, the method fails.
      


        The <i>ppMediaType</i> parameter is optional. If the method fails, the object might use <i>ppMediaType</i> to return a media type that the object does support, and which closely matches the one given in <i>pMediaType</i>. The method is not guaranteed to return a media type in <i>ppMediaType</i>. If no type is returned, this parameter receives a <b>NULL</b> pointer. If the method succeeds, this parameter receives a <b>NULL</b> pointer. If the caller sets <i>ppMediaType</i> to <b>NULL</b>, this parameter is ignored.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>
This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with SP2 and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36">IMFMediaTypeHandler</a>
 

 

