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

# IWMWatermarkInfo::GetWatermarkEntryCount


## -description



The <b>GetWatermarkEntryCount</b> method retrieves the total number of installed watermarking systems of a specified type. Use this method in conjunction with <a href="https://msdn.microsoft.com/7f303233-cd20-40ff-b564-4c44bf17a5f4">IWMWatermarkInfo::GetWatermarkEntry</a> to enumerate the installed watermarking <a href="wmformat_glossary.htm">DMOs</a>.




## -parameters




### -param wmetType [in]

A value from the <a href="https://msdn.microsoft.com/213fcf75-bc15-43a0-aafd-f9cd3c51de93">WMT_WATERMARK_ENTRY_TYPE</a> enumeration type specifying the type of watermarking system..


### -param pdwCount [out]

Pointer to a <b>DWORD</b> containing the number of watermark entries.


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
</table>
 




## -remarks



No watermarking DMOs are provided with the Windows Media Format SDK. You can install third-party DMOs to use with your application.




## -see-also




<a href="https://msdn.microsoft.com/4bdad433-31d1-442c-9701-f3748245070d">IWMWatermarkInfo Interface</a>



<a href="https://msdn.microsoft.com/7f303233-cd20-40ff-b564-4c44bf17a5f4">IWMWatermarkInfo::GetWatermarkEntry</a>
 

 

