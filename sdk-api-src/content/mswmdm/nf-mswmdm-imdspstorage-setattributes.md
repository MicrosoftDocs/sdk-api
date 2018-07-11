---
UID: NF:mswmdm.IMDSPStorage.SetAttributes
title: IMDSPStorage::SetAttributes
author: windows-sdk-content
description: The SetAttributes method sets the attributes of a storage object.
old-location: wmdm\imdspstorage_setattributes.htm
old-project: WMDM
ms.assetid: e995b255-364f-4ea6-b7fd-4443e84432ef
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IMDSPStorage interface [windows Media Device Manager],SetAttributes method, IMDSPStorage.SetAttributes, IMDSPStorage::SetAttributes, IMDSPStorageSetAttributes, SetAttributes, SetAttributes method [windows Media Device Manager], SetAttributes method [windows Media Device Manager],IMDSPStorage interface, mswmdm/IMDSPStorage::SetAttributes, wmdm.imdspstorage_setattributes
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPStorage.SetAttributes
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPStorage::SetAttributes


## -description



The <b>SetAttributes</b> method sets the attributes of a storage object.




## -parameters




### -param dwAttributes [in]

<b>DWORD</b> containing the attributes to be set as defined in the <b>IWMDMStorage::SetAttributes</b> method.


### -param pFormat [in]

Pointer to a <b>_WAVEFORMATEX</b> structure that contains attribute information about the object. This parameter is optional and is ignored if the file is not audio.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



Many of the attributes returned by <b>GetAttributes</b> (as listed in attribute table for <a href="https://msdn.microsoft.com/e43139d2-260a-4f27-a06c-aca741204663">IWMDMStorage::GetAttributes</a>) cannot be set, so they are not listed in the attribute table for <a href="https://msdn.microsoft.com/7484e29a-5faf-4a11-9fc1-75aa5c9d72ef">IWMDMStorage::SetAttributes</a>.

This method is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/fc2fed46-1f4d-4d53-a843-0f699b687a18">IMDSPEnumStorage Interface</a>



<a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage Interface</a>



<a href="https://msdn.microsoft.com/f9c3f7e4-88b1-4842-aaaa-e6c52e1c3116">IMDSPStorage2::SetAttributes2</a>



<a href="https://msdn.microsoft.com/822a5a3f-e649-4e5c-8216-56e77d60a8e3">IMDSPStorage::GetAttributes</a>



<a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a>
 

 

