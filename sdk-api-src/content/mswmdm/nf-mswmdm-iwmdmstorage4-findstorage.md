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

# IWMDMStorage4::FindStorage


## -description



The <b>FindStorage</b> method retrieves a storage in the current root storage, based on its persistent unique identifier.




## -parameters




### -param findScope [in]

A <a href="https://msdn.microsoft.com/971f84d5-8383-4b38-a201-b21100b2f37e">WMDM_FIND_SCOPE</a> enumeration specifying the scope to search.


### -param pwszUniqueID [in]

Persistent unique identifier of the storage to be found. The persistent unique identifier of the storage is described by the <b>g_wszWMDMPersistentUniqueID</b> metadata property of the storage.


### -param ppStorage [out]

Pointer to the retrieved storage, if found. The caller must release this interface when done with it.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method only searches a single memory object (flash card or hard disc) on the device.

A persistent unique identifier identifies content stored on a particular device. It does not represent a content-specific globally unique identifier that remains identical across all devices. Thus, the same content stored in different storages will have different persistent unique identifiers. Similarly, different content may have the same persistent unique identifier when stored on different devices.

The format of the persistent unique identifier depends on the device. The application must have obtained the persistent unique identifier previously by obtaining a storage and querying it for its <b>WMDM/PersistentUniqueID</b> property. Use the <a href="https://msdn.microsoft.com/c4e2c889-9ad0-42d1-bb50-4ebcb9859715">GetSpecifiedMetadata</a> or <a href="https://msdn.microsoft.com/7e436742-fb19-4e8e-98a2-d961c9f0ecbf">GetMetadata</a> methods to request this property.




## -see-also




<a href="https://msdn.microsoft.com/481e6c2d-4103-4818-9ad4-733629af9f9d">IWMDMDevice3::FindStorage</a>



<a href="https://msdn.microsoft.com/7e436742-fb19-4e8e-98a2-d961c9f0ecbf">IWMDMStorage3::GetMetadata</a>



<a href="https://msdn.microsoft.com/ac80cc08-0ff0-48ee-b9c6-e094f803b751">IWMDMStorage4 Interface</a>



<a href="https://msdn.microsoft.com/c4e2c889-9ad0-42d1-bb50-4ebcb9859715">IWMDMStorage4::GetSpecifiedMetadata</a>



<a href="https://msdn.microsoft.com/971f84d5-8383-4b38-a201-b21100b2f37e">WMDM_FIND_SCOPE</a>
 

 

