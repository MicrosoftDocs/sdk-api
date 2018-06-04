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

# TdhLoadManifest function


## -description


Loads the manifest used to decode a log file.


## -parameters




### -param Manifest [in]

The full path to the manifest.


## -returns



Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The manifest file was not found at the specified path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Manifest</i> parameter cannot be <b>NULL</b> and the path cannot exceed MAX_PATH.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_XML_PARSE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The manifest did not pass validation. To determine the validation errors, run the manifest through the message compiler (mc.exe).

</td>
</tr>
</table>
 




## -remarks



To consume events, TDH requires the provider's manifest. Typically, you decode the log file on a computer that contains the provider. Since the provider includes the mainifest as a resource, TDH uses the provider to get the manifest. To decode the log file on a computer that does not contain the provider, you must first use the  TraceRpt.exe executable to export the manifest (see the –export switch) from the provider on a computer that does contain the provider. After you have the manifest file, you can decode the log file on a computer that does not contain the provider.

You need to call this function before decoding the first event. For example, you can call this function before calling the <a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a> function. After processing all the events, call the <a href="https://msdn.microsoft.com/ce0dd781-04b2-4e0c-9e79-44864f53f176">TdhUnloadManifest</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ce0dd781-04b2-4e0c-9e79-44864f53f176">TdhUnloadManifest</a>
 

 

