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

# PdhSelectDataSourceW function


## -description


Displays a dialog window that prompts the user to specify the source of the performance data.
		


## -parameters




### -param hWndOwner [in]

Owner of the dialog window. This can be <b>NULL</b> if there is no owner (the desktop becomes the owner).


### -param dwFlags [in]

Dialog boxes that will be displayed to prompt for the data source. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PDH_FLAGS_FILE_BROWSER_ONLY"></a><a id="pdh_flags_file_browser_only"></a><dl>
<dt><b>PDH_FLAGS_FILE_BROWSER_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Display the file browser only. Set this flag when you want to prompt for the name and location of a log file only.

</td>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Display the data source selection dialog box. The dialog box lets the user select performance data from either a log file or a real-time source. If the user specified that data is to be collected from a log file, a file browser is displayed for the user to specify the name and location of the log file.

</td>
</tr>
</table>
 


### -param szDataSource [out]

Caller-allocated buffer that receives a <b>null</b>-terminated string that contains the name of a log file that the user selected. The log file name is truncated to the size of the buffer if the buffer is too small.

If the user selected a real time source, the buffer is empty.


### -param pcchBufferLength [in, out]

Maximum size of the <i>szDataSource</i> buffer, in <b>TCHARs</b>.


## -returns




						If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. The following are possible values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
The length of the buffer passed in the <i>pcchBufferLength</i> is not equal to the actual length of the <i>szDataSource</i> buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MEMORY_ALLOCATION_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
A zero-length buffer was passed in the <i>szDataSource</i> parameter.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4f6b2d8d-3a0f-4346-8b8e-a7aea11fbc40">PdhIsRealTimeQuery</a>
 

 

