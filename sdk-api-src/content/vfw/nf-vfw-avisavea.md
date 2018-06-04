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

# AVISaveA function


## -description



The <b>AVISave</b> function builds a file by combining data streams from other files or from memory.




## -parameters




### -param szFile

Null-terminated string containing the name of the file to save.


### -param pclsidHandler

Pointer to the file handler used to write the file. The file is created by calling the <a href="https://msdn.microsoft.com/a5d7b278-7c80-42a3-94a4-5c012ad9a9fd">AVIFileOpen</a> function using this handler. If a handler is not specified, a default is selected from the registry based on the file extension.


### -param lpfnCallback

Pointer to a callback function for the save operation.


### -param nStreams

Number of streams saved in the file.


### -param pfile

TBD


### -param lpOptions

Pointer to an application-defined <a href="https://msdn.microsoft.com/8084adc3-792f-4a6c-b407-51e0e435e629">AVICOMPRESSOPTIONS</a> structure containing the compression options for the stream referenced by <i>pavi</i>. This parameter is paired with pavi. The parameter pair can be repeated as a variable number of arguments.


### -param param

TBD






#### - pavi

Pointer to an AVI stream. This parameter is paired with <i>lpOptions</i>. The parameter pair can be repeated as a variable number of arguments.


## -returns



Returns AVIERR_OK if successful or an error otherwise.




## -remarks



This function creates a file, copies stream data into the file, closes the file, and releases the resources used by the new file. The last two parameters of this function identify a stream to save in the file and define the compression options of that stream. When saving more than one stream in an AVI file, repeat these two stream-specific parameters for each stream in the file.

A callback function (referenced by using <i>lpfnCallback</i>) can display status information and let the user cancel the save operation. The callback function uses the following format:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
LONG PASCAL SaveCallback(int nPercent)  
</pre>
</td>
</tr>
</table></span></div>
The <i>nPercent</i> parameter specifies the percentage of the file saved.

The callback function should return AVIERR_OK if the operation should continue and AVIERR_USERABORT if the user wishes to abort the save operation.

The argument <i>pavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

