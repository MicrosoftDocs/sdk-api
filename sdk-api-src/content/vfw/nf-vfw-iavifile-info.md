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

# IAVIFile::Info


## -description



The <b>Info</b> method returns with information about an AVI file. Called when an application uses the <a href="https://msdn.microsoft.com/10d7decf-a133-4d55-93d5-867952307819">AVIFileInfo</a> function.




## -parameters




### -param pfi


            A pointer to an <a href="https://msdn.microsoft.com/d3fda342-2ade-41b1-b709-c194f132e015">AVIFILEINFO</a> structure. The method fills the structure with information about the file.


### -param lSize

The size, in bytes, of the buffer specified by <i>pfi</i>.


#### - pf


            Pointer to the interface to a file.
          


## -returns




            Returns the HRESULT defined by OLE.
          




## -remarks



If the buffer allocated is too small for the structure, this method should fail the call by returning AVIERR_BUFFERTOOSMALL. Otherwise, it should fill the structure and return its size.

For handlers written in C++, <b>Info</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT Info(AVIFILEINFO *pfi, LONG lSize) 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

