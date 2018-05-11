---
UID: NF:mswmdm.IWMDMEnumStorage.Skip
title: IWMDMEnumStorage::Skip
author: windows-driver-content
description: The Skip method skips over the specified number of storages in the enumeration sequence.
old-location: wmdm\iwmdmenumstorage_skip.htm
old-project: WMDM
ms.assetid: 0073f279-95e4-41e3-9195-c4c93fd41fb6
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWMDMEnumStorage interface [windows Media Device Manager],Skip method, IWMDMEnumStorage.Skip, IWMDMEnumStorage::Skip, IWMDMEnumStorageSkip, Skip, Skip method [windows Media Device Manager], Skip method [windows Media Device Manager],IWMDMEnumStorage interface, mswmdm/IWMDMEnumStorage::Skip, wmdm.iwmdmenumstorage_skip
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
-	IWMDMEnumStorage.Skip
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IWMDMEnumStorage::Skip


## -description



The <b>Skip</b> method skips over the specified number of storages in the enumeration sequence.




## -parameters




### -param celt [in]

The number of storages to skip.


### -param pceltFetched [out]

The number of storages skipped.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



If the number of devices specified in <i>celt</i> is greater than the actual number of storage interfaces remaining in the enumeration sequence, this function will return S_FALSE. When this happens, <i>pceltFetched</i> must be queried to determine how many interfaces were actually skipped. If you skip to the end of the array of storage interfaces, a subsequent call to <b>Next</b> returns S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/6ea80ab2-718b-464e-a805-9910460931bb">IWMDMEnumStorage Interface</a>
 

 

