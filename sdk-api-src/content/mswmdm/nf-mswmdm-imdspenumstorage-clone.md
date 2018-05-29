---
UID: NF:mswmdm.IMDSPEnumStorage.Clone
title: IMDSPEnumStorage::Clone
author: windows-sdk-content
description: The Clone method creates another enumerator that contains the same enumeration state as the current one.
old-location: wmdm\imdspenumstorage_clone.htm
old-project: WMDM
ms.assetid: 8621c5fa-7739-4f90-b856-76880f8dd07b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: Clone, Clone method [windows Media Device Manager], Clone method [windows Media Device Manager],IMDSPEnumStorage interface, IMDSPEnumStorage interface [windows Media Device Manager],Clone method, IMDSPEnumStorage.Clone, IMDSPEnumStorage::Clone, IMDSPEnumStorageClone, mswmdm/IMDSPEnumStorage::Clone, wmdm.imdspenumstorage_clone
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
-	IMDSPEnumStorage.Clone
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPEnumStorage::Clone


## -description



The <b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one.




## -parameters




### -param ppEnumStorage [out]

Pointer to an <a href="https://msdn.microsoft.com/fc2fed46-1f4d-4d53-a843-0f699b687a18">IMDSPEnumStorage</a> interface.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



Using this function, a client can record a particular point in the enumeration sequence, and return to that point at a later time. The new enumerator supports the same interface as the original one.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/fc2fed46-1f4d-4d53-a843-0f699b687a18">IMDSPEnumStorage Interface</a>
 

 

