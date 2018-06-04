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

# IWMDMStorage::GetSize


## -description



The <b>GetSize</b> method retrieves the size of the storage, in bytes.




## -parameters




### -param pdwSizeLow [out]

Pointer to a <b>DWORD</b> specifying the low-order part of the storage object size, in bytes.


### -param pdwSizeHigh [out]

Pointer to a <b>DWORD</b> specifying the high-order part of the storage object size, in bytes.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



For folders or abstract objects (such as abstract playlists), the size is zero.


#### Examples

The following C++ code retrieves the size of a file, in kilobytes.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Get size of file in kilobytes.
DWORD lowSize = 0;
DWORD highSize = 0;
hr = pStorage-&gt;GetSize(&amp;lowSize, &amp;highSize);
//TODO: Display the file size.
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>



<a href="https://msdn.microsoft.com/53693e2f-f6d2-42cc-9387-798f8dc10556">IWMDMStorage::GetDate</a>



<a href="https://msdn.microsoft.com/1387a82f-e320-402a-b3c9-2f28550c4caf">IWMDMStorage::GetName</a>
 

 

