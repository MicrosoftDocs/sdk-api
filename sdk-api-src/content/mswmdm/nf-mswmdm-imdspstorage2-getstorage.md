---
UID: NF:mswmdm.IMDSPStorage2.GetStorage
title: IMDSPStorage2::GetStorage
author: windows-sdk-content
description: The GetStorage method makes it possible to go directly to a storage object from a storage name instead of enumerating through all storages to find it.
old-location: wmdm\imdspstorage2_getstorage.htm
old-project: WMDM
ms.assetid: 2ddfdfc8-db43-4acc-aebc-617d3e746a4f
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetStorage, GetStorage method [windows Media Device Manager], GetStorage method [windows Media Device Manager],IMDSPStorage2 interface, IMDSPStorage2 interface [windows Media Device Manager],GetStorage method, IMDSPStorage2.GetStorage, IMDSPStorage2::GetStorage, IMDSPStorage2GetStorage, mswmdm/IMDSPStorage2::GetStorage, wmdm.imdspstorage2_getstorage
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
-	IMDSPStorage2.GetStorage
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPStorage2::GetStorage


## -description



The <b>GetStorage</b> method makes it possible to go directly to a storage object from a storage name instead of enumerating through all storages to find it.




## -parameters




### -param pszStorageName [in]

Pointer to a <b>null</b>-terminated string containing the storage name.


### -param ppStorage [out]

Pointer to the storage object specified by <i>pszStorageName</i>, or <b>NULL</b> if no such storage was found.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The <b>IMDSPStorage2::GetStorage</b> interface extends the functionality of <b>IMDSPStorage</b>.

<b>IMDSPStorage2::GetStorage</b> does not support wildcard characters. It is not recursive, that is, it will only find storage objects in the current storage.

If this method is not implemented, it should return E_NOTIMPL. (It should not return WMDM_E_NOT_SUPPORTED or any other codes indicating that this method is not implemented). This will ensure that Windows Media Device Manager will attempt to substitute this functionality itself by enumerating all storages to find a match based on the storage name passed in as <i>pszStorageName</i>.

It is strongly recommended that a service provider implement this method to efficiently return a storage object based on name.

This method is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage Interface</a>



<a href="https://msdn.microsoft.com/39afb282-7141-4eb5-93e9-a69bef495d80">IMDSPStorage2 Interface</a>
 

 

