---
UID: NF:mswmdm.IWMDMStorage4.FindStorage
title: IWMDMStorage4::FindStorage method
author: windows-driver-content
description: The FindStorage method retrieves a storage in the current root storage, based on its persistent unique identifier.
old-location: wmdm\iwmdmstorage4_findstorage.htm
old-project: WMDM
ms.assetid: 93ca4488-beaf-4617-99ba-19bb7707d4ba
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: FindStorage method [windows Media Device Manager], FindStorage method [windows Media Device Manager], IWMDMStorage4 interface, FindStorage,IWMDMStorage4.FindStorage, IWMDMStorage4, IWMDMStorage4 interface [windows Media Device Manager], FindStorage method, IWMDMStorage4::FindStorage, IWMDMStorage4FindStorage, mswmdm/IWMDMStorage4::FindStorage, wmdm.iwmdmstorage4_findstorage
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
-	IWMDMStorage4.FindStorage
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IWMDMStorage4::FindStorage method


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
 

 

