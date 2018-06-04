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

# IAVIStream::FindSample


## -description



The <b>FindSample</b> method obtains the position in a stream of a key frame or a nonempty frame. Called when an application uses the <a href="https://msdn.microsoft.com/2bd89f50-0d3a-4c34-b7b8-dc29f2d54d55">AVIStreamFindSample</a> function.




## -parameters




### -param lPos

Position of the sample or frame.


### -param lFlags

Applicable flags. The following values are defined.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>FIND_ANY</td>
<td>Searches for a nonempty frame.</td>
</tr>
<tr>
<td>FIND_FORMAT</td>
<td>Searches for a format change.</td>
</tr>
<tr>
<td>FIND_KEY</td>
<td>Searches for a key frame.</td>
</tr>
<tr>
<td>FIND_NEXT</td>
<td>Searches forward through a stream, beginning with the current frame.</td>
</tr>
<tr>
<td>FIND_PREV</td>
<td>Searches backward through a stream, beginning with the current frame.</td>
</tr>
</table>
 

The FIND_ANY, FIND_KEY, and FIND_FORMAT flags are mutually exclusive, as are the FIND_NEXT and FIND_PREV flags. You must specify one value from each group.


#### - ps

Pointer to the interface to a stream.


## -returns



Returns the location of the key frame corresponding to the frame specified by the application.




## -remarks



If key frames are not significant in your custom format, return the position specified for <i>lPos</i>.

For handlers written in C++, <b>FindSample</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
LONG FindSample(LONG lPos, LONG lFlags) 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

