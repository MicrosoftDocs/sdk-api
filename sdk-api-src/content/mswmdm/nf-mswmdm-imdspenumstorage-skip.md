---
UID: NF:mswmdm.IMDSPEnumStorage.Skip
title: IMDSPEnumStorage::Skip (mswmdm.h)
author: windows-sdk-content
description: The Skip method skips over the next specified number of storage interface(s) in the enumeration sequence.
old-location: wmdm\imdspenumstorage_skip.htm
tech.root: WMDM
ms.assetid: 68025a40-a423-4a11-87c6-ae8c2d7b3765
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMDSPEnumStorage interface [windows Media Device Manager],Skip method, IMDSPEnumStorage.Skip, IMDSPEnumStorage::Skip, IMDSPEnumStorageSkip, Skip, Skip method [windows Media Device Manager], Skip method [windows Media Device Manager],IMDSPEnumStorage interface, mswmdm/IMDSPEnumStorage::Skip, wmdm.imdspenumstorage_skip
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPEnumStorage.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPEnumStorage::Skip


## -description



The <b>Skip</b> method skips over the next specified number of storage interface(s) in the enumeration sequence.




## -parameters




### -param celt [in]

Number of elements to skip.


### -param pceltFetched [out]

Pointer to the number of elements actually skipped.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



If the number specified in the <i>celt</i> parameter is greater than the actual number of storage interfaces remaining in the enumeration sequence, the return value from <b>Skip</b> is S_FALSE. When this happens, the <i>pceltFetched</i> parameter must be queried to determine how many interfaces were skipped. If you skip to the end of the array of storage interfaces, a subsequent call to <b>Next</b> returns S_FALSE.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/fc2fed46-1f4d-4d53-a843-0f699b687a18">IMDSPEnumStorage Interface</a>
 

 

