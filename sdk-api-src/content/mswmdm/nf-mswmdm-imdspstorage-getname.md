---
UID: NF:mswmdm.IMDSPStorage.GetName
title: IMDSPStorage::GetName
author: windows-sdk-content
description: The GetName method retrieves the display name of the storage object.
old-location: wmdm\imdspstorage_getname.htm
old-project: WMDM
ms.assetid: 6172f222-8b92-4da5-8001-b79431c26518
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetName, GetName method [windows Media Device Manager], GetName method [windows Media Device Manager],IMDSPStorage interface, IMDSPStorage interface [windows Media Device Manager],GetName method, IMDSPStorage.GetName, IMDSPStorage::GetName, IMDSPStorageGetName, mswmdm/IMDSPStorage::GetName, wmdm.imdspstorage_getname
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
 - IMDSPStorage.GetName
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPStorage::GetName


## -description



The <b>GetName</b> method retrieves the display name of the storage object.




## -parameters




### -param pwszName [out]

Pointer to a (Unicode) wide-character null-terminated string containing the object name.


### -param nMaxChars [in]

Integer containing the maximum number of characters that can be copied to the name string.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The display name of the object is the file name without path information. In hierarchical media the display name would be concatenated with the ancestor instances of <b>IMDSPStorage</b> interfaces to create a full path-qualified name.

The <b>LPWSTR</b> string type is a 16-bit Unicode character string and does not accept byte-sized characters.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage Interface</a>



<a href="https://msdn.microsoft.com/4ba0c598-9ea2-42cc-a234-1c0e192971a8">IMDSPStorage::GetDate</a>



<a href="https://msdn.microsoft.com/95b28f9a-744c-4d49-a91c-6652d688b91a">IMDSPStorage::GetSize</a>
 

 

