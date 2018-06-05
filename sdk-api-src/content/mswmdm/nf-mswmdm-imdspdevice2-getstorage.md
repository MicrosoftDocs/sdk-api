---
UID: NF:mswmdm.IMDSPDevice2.GetStorage
title: IMDSPDevice2::GetStorage
author: windows-sdk-content
description: The GetStorage method makes it possible to go directly to a storage based on its name instead of enumerating through all storages to find it.
old-location: wmdm\imdspdevice2_getstorage.htm
old-project: WMDM
ms.assetid: d01cf5a6-1fdb-4354-8b43-b04bdc562d71
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetStorage, GetStorage method [windows Media Device Manager], GetStorage method [windows Media Device Manager],IMDSPDevice2 interface, IMDSPDevice2 interface [windows Media Device Manager],GetStorage method, IMDSPDevice2.GetStorage, IMDSPDevice2::GetStorage, IMDSPDevice2GetStorage, mswmdm/IMDSPDevice2::GetStorage, wmdm.imdspdevice2_getstorage
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
-	IMDSPDevice2.GetStorage
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPDevice2::GetStorage


## -description



The <b>GetStorage</b> method makes it possible to go directly to a storage based on its name instead of enumerating through all storages to find it.




## -parameters




### -param pszStorageName [in]

Pointer to a null-terminated string containing the name of the storage to find.


### -param ppStorage [out]

Pointer to the storage object specified by the <i>pszStorageName</i> parameter.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The <b>GetStorage</b> method does not support wildcard characters. It is not recursive, that is, it will only find storages in the root of the device.

If this method is not implemented, it should return E_NOTIMPL. (It should not return WMDM_E_NOT_SUPPORTED or any other codes indicating that this method is not implemented). This will ensure that Windows Media Device Manager will attempt to substitute this functionality itself by enumerating all storages to find a match based on the storage name passed in as <i>pszStorageName</i>.

It is strongly recommended that a service provider implement this method to efficiently return a storage object based on name.

This method is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/a53052a1-89f4-4571-9eee-031e0049a92e">IMDSPDevice2 Interface</a>
 

 

