---
UID: NF:mswmdm.IWMDMStorage.GetStorageGlobals
title: IWMDMStorage::GetStorageGlobals
author: windows-sdk-content
description: The GetStorageGlobals method retrieves the IWMDMStorageGlobals interface of the root storage of this storage.
old-location: wmdm\iwmdmstorage_getstorageglobals.htm
old-project: WMDM
ms.assetid: 0203f881-f838-412b-a796-42f946513c65
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetStorageGlobals, GetStorageGlobals method [windows Media Device Manager], GetStorageGlobals method [windows Media Device Manager],IWMDMStorage interface, IWMDMStorage interface [windows Media Device Manager],GetStorageGlobals method, IWMDMStorage.GetStorageGlobals, IWMDMStorage::GetStorageGlobals, IWMDMStorageGetStorageGlobals, mswmdm/IWMDMStorage::GetStorageGlobals, wmdm.iwmdmstorage_getstorageglobals
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
-	IWMDMStorage.GetStorageGlobals
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorage::GetStorageGlobals


## -description



The <b>GetStorageGlobals</b> method retrieves the <b>IWMDMStorageGlobals</b> interface of the root storage of this storage.




## -parameters




### -param ppStorageGlobals [out]

Pointer to an <a href="https://msdn.microsoft.com/fe164271-58f0-4b28-a200-6b15f8b42d36">IWMDMStorageGlobals</a> interface, which provides information about the device such as serial number, capabilities, and so on. The caller must release this interface when finished with it.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The <b>IWMDMStorageGlobals</b> interface returned provides methods for accessing global information about the root storage of the current storage. Because this interface exposes global device information, an application only needs to call this method once, on any storage within a single memory container.




## -see-also




<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>



<a href="https://msdn.microsoft.com/fe164271-58f0-4b28-a200-6b15f8b42d36">IWMDMStorageGlobals Interface</a>
 

 

