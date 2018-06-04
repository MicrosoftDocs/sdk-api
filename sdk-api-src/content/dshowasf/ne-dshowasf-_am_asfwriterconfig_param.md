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

# _AM_ASFWRITERCONFIG_PARAM enumeration


## -description



Defines configuration parameters for the <a href="https://msdn.microsoft.com/1b12f65f-8d77-4d38-aad9-92bb15cc0426">WM ASF Writer</a> filter.




## -enum-fields




### -field AM_CONFIGASFWRITER_PARAM_AUTOINDEX

Specifies whether the <a href="https://msdn.microsoft.com/1b12f65f-8d77-4d38-aad9-92bb15cc0426">WM ASF Writer</a> automatically creates a temporal index after it has completed encoding a file. Set this parameter to <b>FALSE</b> if you want to create a frame-based index using the Windows Media Format SDK directly.


### -field AM_CONFIGASFWRITER_PARAM_MULTIPASS

Specifies whether the filter operates in two-pass mode. See Remarks.


### -field AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS

If <b>TRUE</b>, specifies that the <a href="https://msdn.microsoft.com/1b12f65f-8d77-4d38-aad9-92bb15cc0426">WM ASF Writer</a> will not attempt to compress the input streams. Use this flag to write content that is not Windows Media–based into an ASF file.


## -remarks



In two-pass mode, the filter makes two passes through the file. In the first pass, the filter examines each media stream in its entirety to determine the optimal encoding parameters for the file. The actual encoding is performed in the second pass. Therefore, to create an ASF file in two-pass mode, you must run the graph, wait for an <a href="https://msdn.microsoft.com/2029afc4-419c-494a-ae52-1f84b08bcb35">EC_PREPROCESS_COMPLETE</a> event, seek to the beginning of the source file, and then run the graph a second time.

<div class="alert"><b>Important</b>  To receive the <b>EC_PREPROCESS_COMPLETE</b> event, you must call <a href="https://msdn.microsoft.com/d7cbbf6d-c741-416f-b8dd-d9ca012d309a">IMediaEvent::GetEvent</a>. The <a href="https://msdn.microsoft.com/760a90fe-7cbc-4f09-ba64-afe0ab0b4c74">IMediaEvent::WaitForCompletion</a> method does not respond to this event.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/2a875d02-3814-46a1-9eee-61bad36475fc">IConfigAsfWriter2::GetParam</a>



<a href="https://msdn.microsoft.com/0294837c-0cf2-4a05-bef4-16d13864f759">IConfigAsfWriter2::SetParam</a>
 

 

