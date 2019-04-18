---
UID: NF:mswmdm.IWMDMStorageGlobals.GetTotalFree
title: IWMDMStorageGlobals::GetTotalFree (mswmdm.h)
author: windows-sdk-content
description: The GetTotalFree method retrieves the total amount of free space on the storage medium, in bytes.
old-location: wmdm\iwmdmstorageglobals_gettotalfree.htm
tech.root: WMDM
ms.assetid: a97c2d92-dc54-4987-b2b4-e4de2e546a1f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTotalFree, GetTotalFree method [windows Media Device Manager], GetTotalFree method [windows Media Device Manager],IWMDMStorageGlobals interface, IWMDMStorageGlobals interface [windows Media Device Manager],GetTotalFree method, IWMDMStorageGlobals.GetTotalFree, IWMDMStorageGlobals::GetTotalFree, IWMDMStorageGlobalsGetTotalFree, mswmdm/IWMDMStorageGlobals::GetTotalFree, wmdm.iwmdmstorageglobals_gettotalfree
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
 - IWMDMStorageGlobals.GetTotalFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMStorageGlobals::GetTotalFree


## -description



The <b>GetTotalFree</b> method retrieves the total amount of free space on the storage medium, in bytes.




## -parameters




### -param pdwFreeLow [out]

Pointer to a <b>DWORD</b> that receives the low-order part of the free space value.


### -param pdwFreeHigh [out]

Pointer to a <b>DWORD</b> that receives the high-order part of the free space value.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



To determine the amount of storage space in use by the medium for file management, subtract the number of bad bytes retrieved using <a href="https://msdn.microsoft.com/40e1a39b-2757-472c-b585-77b829605e8c">GetTotalBad</a> from the number of free bytes retrieved using <b>GetTotalFree</b>.




## -see-also




<a href="https://msdn.microsoft.com/fe164271-58f0-4b28-a200-6b15f8b42d36">IWMDMStorageGlobals Interface</a>



<a href="https://msdn.microsoft.com/40e1a39b-2757-472c-b585-77b829605e8c">IWMDMStorageGlobals::GetTotalBad</a>



<a href="https://msdn.microsoft.com/ebbc8b7e-037f-4b8d-b026-793d38914685">IWMDMStorageGlobals::GetTotalSize</a>
 

 

