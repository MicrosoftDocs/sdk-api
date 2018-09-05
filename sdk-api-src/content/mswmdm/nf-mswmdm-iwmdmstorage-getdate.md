---
UID: NF:mswmdm.IWMDMStorage.GetDate
title: IWMDMStorage::GetDate
author: windows-sdk-content
description: The GetDate method retrieves the date when the storage was last modified.
old-location: wmdm\iwmdmstorage_getdate.htm
old-project: WMDM
ms.assetid: 53693e2f-f6d2-42cc-9387-798f8dc10556
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetDate, GetDate method [windows Media Device Manager], GetDate method [windows Media Device Manager],IWMDMStorage interface, IWMDMStorage interface [windows Media Device Manager],GetDate method, IWMDMStorage.GetDate, IWMDMStorage::GetDate, IWMDMStorageGetDate, mswmdm/IWMDMStorage::GetDate, wmdm.iwmdmstorage_getdate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMStorage.GetDate
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorage::GetDate


## -description



The <b>GetDate</b> method retrieves the date when the storage was last modified.




## -parameters




### -param pDateTimeUTC [out]

Pointer to a <b>WMDMDATETIME</b> structure specifying the date on which the storage object (file or folder) was last modified.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The time is specified in coordinated universal time.


#### Examples

The following C++ code gets the "last modified" value from a storage passed in.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Get the "Last Modified" date
WMDMDATETIME lastModified;
hr = pStorage-&gt;GetDate(&amp;lastModified);
// TODO: Display the last modified month, day, and year.
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>
 

 

