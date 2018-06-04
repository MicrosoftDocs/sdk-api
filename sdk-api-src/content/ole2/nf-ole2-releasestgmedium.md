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

# ReleaseStgMedium function


## -description


Frees the specified storage medium.


## -parameters




### -param LPSTGMEDIUM

TBD




#### - pMedium [in]

Pointer to the storage medium that is to be freed.


## -returns



This function does not return a value.




## -remarks



The <b>ReleaseStgMedium</b> function calls the appropriate method or function to release the specified storage medium. Use this function during data transfer operations where storage medium structures are parameters, such as <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a> or <a href="https://msdn.microsoft.com/7430d12c-ab07-4a9c-a845-4743818afbc7">IDataObject::SetData</a>. In addition to identifying the type of the storage medium, this structure specifies the appropriate <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method for releasing the storage medium when it is no longer needed.

It is common to pass a <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> from one body of code to another, such as in <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a>, in which the one called can allocate a medium and return it to the caller. <b>ReleaseStgMedium</b> permits flexibility in whether the receiving body of code owns the medium, or whether the original provider of the medium still owns it, in which case the receiving code needs to inform the provider that it can free the medium.

When the original provider of the medium is responsible for freeing the medium, the provider calls <b>ReleaseStgMedium</b>, specifying the medium and the appropriate <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer as the <b>punkForRelease</b> structure member. Depending on the type of storage medium being freed, one of the following actions is taken, followed by a call to the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the specified <b>IUnknown</b> pointer.

<table>
<tr>
<th>Medium</th>
<th>ReleaseStgMedium Action</th>
</tr>
<tr>
<td>TYMED_HGLOBAL</td>
<td>None.</td>
</tr>
<tr>
<td>TYMED_GDI</td>
<td>None.</td>
</tr>
<tr>
<td>TYMED_ENHMF</td>
<td>None.</td>
</tr>
<tr>
<td>TYMED_MFPICT</td>
<td>None.</td>
</tr>
<tr>
<td>TYMED_FILE</td>
<td>Frees the file name string using standard memory management mechanisms.</td>
</tr>
<tr>
<td>TYMED_ISTREAM</td>
<td>Calls <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IStream::Release</a>.</td>
</tr>
<tr>
<td>TYMED_ISTORAGE</td>
<td>Calls <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IStorage::Release</a>.</td>
</tr>
</table>
 

The provider indicates that the receiver of the medium is responsible for freeing the medium by specifying <b>NULL</b> for the <b>punkForRelease</b> structure member. Then the receiver calls <b>ReleaseStgMedium</b>, which makes a call as described in the following table depending on the type of storage medium being freed.

<table>
<tr>
<th>Medium</th>
<th>ReleaseStgMedium Action</th>
</tr>
<tr>
<td>TYMED_HGLOBAL</td>
<td>Calls the <a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a> function on the handle.</td>
</tr>
<tr>
<td>TYMED_GDI</td>
<td>Calls the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function on the handle.</td>
</tr>
<tr>
<td>TYMED_ENHMF</td>
<td>Deletes the enhanced metafile.</td>
</tr>
<tr>
<td>TYMED_MFPICT</td>
<td>The hMF that it contains is deleted with the <a href="https://msdn.microsoft.com/51766282-f185-4e29-a36e-1069d9d61f7c">DeleteMetaFile</a> function; then the handle itself is passed to <a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a>.</td>
</tr>
<tr>
<td>TYMED_FILE</td>
<td>Frees the disk file by deleting it. Frees the file name string by using the standard memory management mechanisms.</td>
</tr>
<tr>
<td>TYMED_ISTREAM</td>
<td>Calls <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IStream::Release</a>.</td>
</tr>
<tr>
<td>TYMED_ISTORAGE</td>
<td>Calls <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IStorage::Release</a>.</td>
</tr>
</table>
 

In either case, after the call to <b>ReleaseStgMedium</b>, the specified storage medium is invalid and can no longer be used.




## -see-also




<a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a>
 

 

