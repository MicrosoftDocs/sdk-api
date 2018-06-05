---
UID: NF:mswmdm.IWMDMStorage.GetSize
title: IWMDMStorage::GetSize
author: windows-sdk-content
description: The GetSize method retrieves the size of the storage, in bytes.
old-location: wmdm\iwmdmstorage_getsize.htm
old-project: WMDM
ms.assetid: 1042b71b-1656-4f0b-be95-8a09ba4421ed
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetSize, GetSize method [windows Media Device Manager], GetSize method [windows Media Device Manager],IWMDMStorage interface, IWMDMStorage interface [windows Media Device Manager],GetSize method, IWMDMStorage.GetSize, IWMDMStorage::GetSize, IWMDMStorageGetSize, mswmdm/IWMDMStorage::GetSize, wmdm.iwmdmstorage_getsize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMStorage.GetSize
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

