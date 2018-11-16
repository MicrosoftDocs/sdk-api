---
UID: NF:mswmdm.IWMDMStorage.EnumStorage
title: IWMDMStorage::EnumStorage
author: windows-sdk-content
description: The EnumStorage method retrieves an IWMDMEnumStorage interface to enumerate the immediate child storages of the current storage.
old-location: wmdm\iwmdmstorage_enumstorage.htm
tech.root: WMDM
ms.assetid: ab3c6a17-5a86-419b-b528-fd0db718de8f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EnumStorage, EnumStorage method [windows Media Device Manager], EnumStorage method [windows Media Device Manager],IWMDMStorage interface, IWMDMStorage interface [windows Media Device Manager],EnumStorage method, IWMDMStorage.EnumStorage, IWMDMStorage::EnumStorage, IWMDMStorageEnumStorage, mswmdm/IWMDMStorage::EnumStorage, wmdm.iwmdmstorage_enumstorage
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
 - IWMDMStorage.EnumStorage
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
- IWMDMStorage.EnumStorage
: 
---

# IWMDMStorage::EnumStorage


## -description



The <b>EnumStorage</b> method retrieves an <b>IWMDMEnumStorage</b> interface to enumerate the immediate child storages of the current storage.




## -parameters




### -param pEnumStorage [out]

Pointer to an <a href="https://msdn.microsoft.com/6ea80ab2-718b-464e-a805-9910460931bb">IWMDMEnumStorage</a> interface. The caller must release this interface when done with it.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The <b>IWMDMEnumStorage</b> interface that is retrieved will enumerate the immediate chilren of this object. This method allows an application to navigate the contents of a device recursively.




## -see-also




<a href="https://msdn.microsoft.com/8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0">Exploring a Device</a>



<a href="https://msdn.microsoft.com/ffd3c51a-7ec2-4ce5-9260-2b08bfa88a99">IWMDMDevice::EnumStorage</a>



<a href="https://msdn.microsoft.com/6ea80ab2-718b-464e-a805-9910460931bb">IWMDMEnumStorage Interface</a>



<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>
 

 

