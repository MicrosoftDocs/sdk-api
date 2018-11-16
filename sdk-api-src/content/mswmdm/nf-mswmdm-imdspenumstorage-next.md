---
UID: NF:mswmdm.IMDSPEnumStorage.Next
title: IMDSPEnumStorage::Next
author: windows-sdk-content
description: The Next method returns a pointer to the next celtIMDSPStorage interfaces.
old-location: wmdm\imdspenumstorage_next.htm
tech.root: WMDM
ms.assetid: 7874912a-6350-445c-a7c8-0f885d756aa0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMDSPEnumStorage interface [windows Media Device Manager],Next method, IMDSPEnumStorage.Next, IMDSPEnumStorage::Next, IMDSPEnumStorageNext, Next, Next method [windows Media Device Manager], Next method [windows Media Device Manager],IMDSPEnumStorage interface, mswmdm/IMDSPEnumStorage::Next, wmdm.imdspenumstorage_next
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMDSPEnumStorage.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mswmdm.h
: 
- IMDSPEnumStorage.Next
: 
---

# IMDSPEnumStorage::Next


## -description



The <b>Next</b> method returns a pointer to the next <i>celt</i><a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage</a> interfaces.




## -parameters




### -param celt [in]

Number of storage interfaces requested.


### -param ppStorage [out]

Array of <i>celt</i><a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage</a> interface pointers allocated by the caller. Return <b>NULL</b> if no more storage media exist, or an error has occurred. If <i>celt</i> is more than 1, the caller must allocate enough memory to store <i>celt</i> number of interface pointers.


### -param pceltFetched [out]

Pointer to a <b>ULONG</b> variable that receives the count of interfaces returned.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



When there are no more storage interfaces, or when there are fewer storage interfaces than requested, the return value from <b>Next</b> is S_FALSE. When this happens, the <i>pceltFetched</i> parameter must be queried to determine how many interfaces, if any, were returned.

The storage enumerator may not reflect the effect of media insertion and removal. In such cases, the client should obtain a new enumerator object.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/fc2fed46-1f4d-4d53-a843-0f699b687a18">IMDSPEnumStorage Interface</a>



<a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage Interface</a>



<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>
 

 

