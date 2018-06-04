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

# IWMDMStorage3::SetMetadata


## -description



The <b>SetMetadata</b> method sets metadata on the storage.




## -parameters




### -param pMetadata [in]

An <a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData</a> pointer containing metadata to set on the object. To create this interface, call <a href="https://msdn.microsoft.com/e46b5f30-3dd9-4e5a-bd75-c7716a1d8a2a">CreateEmptyMetadataObject</a>.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



Existing properties in the storage with the same name are overwritten. All other existing properties are not modified or lost.

To set properties for a Windows Portable Devices (WPD) device, an application would create an <b>IPortableDeviceValues</b> object and set each property into this collection. Then, the application would serialize the collection to a binary large object (BLOB). Once the data is serialized, the application would add it to the <b>IWMDMMetaData</b> referenced by the <i>pMetadata</i> argument using the g_wszWPDPassthroughPropertyValues metadata constant.


#### Examples

The following C++ code adds a subtitle as metadata to a storage (pStorage3) using the <b>IWMDMMetaData</b> interface retrieved from the storage previously (not shown).

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Set metadata values on a storage.
WCHAR* station = L"Mysubtitle";
UINT numBytes = (wcslen(station) + 1) * sizeof(WCHAR); // WCHAR string is 2 * length of characters long
                                                       // plus the terminating null character.
hr = pMetadata-&gt;AddItem(WMDM_TYPE_STRING, g_wszWMDMMediaStationName, (BYTE*)station, numBytes) ;
BREAK_HR(hr, "Added a metadata value to the interface in TestUpdateMetadata.", "Couldn't add a metadata value to the interface in TestUpdateMetadata.");

// Add the metadata to the storage.
hr = pStorage3-&gt;SetMetadata(pMetadata);
BREAK_HR(hr, "Set metadata on the storage in TestUpdateMetadata.", "Couldn't set metadata on the storage in TestUpdateMetadata: " &lt;&lt; hex &lt;&lt; hr &lt;&lt; dec);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData Interface</a>



<a href="https://msdn.microsoft.com/b62ea18b-c692-464f-a009-727a2924f8b8">IWMDMStorage3 Interface</a>



<a href="https://msdn.microsoft.com/7e436742-fb19-4e8e-98a2-d961c9f0ecbf">IWMDMStorage3::GetMetadata</a>



<a href="https://msdn.microsoft.com/478a5412-e8b4-41c8-802f-9c2748dbaeae">Setting Metadata on a File</a>
 

 

