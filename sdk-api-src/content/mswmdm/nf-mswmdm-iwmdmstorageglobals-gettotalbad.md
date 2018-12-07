---
UID: NF:mswmdm.IWMDMStorageGlobals.GetTotalBad
title: IWMDMStorageGlobals::GetTotalBad
author: windows-sdk-content
description: The GetTotalBad method retrieves the total amount of unusable space on the storage medium, in bytes.
old-location: wmdm\iwmdmstorageglobals_gettotalbad.htm
tech.root: WMDM
ms.assetid: 40e1a39b-2757-472c-b585-77b829605e8c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTotalBad, GetTotalBad method [windows Media Device Manager], GetTotalBad method [windows Media Device Manager],IWMDMStorageGlobals interface, IWMDMStorageGlobals interface [windows Media Device Manager],GetTotalBad method, IWMDMStorageGlobals.GetTotalBad, IWMDMStorageGlobals::GetTotalBad, IWMDMStorageGlobalsGetTotalBad, mswmdm/IWMDMStorageGlobals::GetTotalBad, wmdm.iwmdmstorageglobals_gettotalbad
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
 - IWMDMStorageGlobals.GetTotalBad
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMStorageGlobals::GetTotalBad


## -description



The <b>GetTotalBad</b> method retrieves the total amount of unusable space on the storage medium, in bytes.




## -parameters




### -param pdwBadLow [out]

Pointer to a <b>DWORD</b> that receives the low-order bytes of unusable space.


### -param pdwBadHigh [out]

Pointer to a <b>DWORD</b> that receives the high-order bytes of unusable space.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



To determine the amount of storage space in use by the medium for file management, subtract the number of bad bytes retrieved using <b>GetTotalBad</b> from the number of free bytes retrieved using <a href="https://msdn.microsoft.com/a97c2d92-dc54-4987-b2b4-e4de2e546a1f">GetTotalFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/fe164271-58f0-4b28-a200-6b15f8b42d36">IWMDMStorageGlobals Interface</a>



<a href="https://msdn.microsoft.com/a97c2d92-dc54-4987-b2b4-e4de2e546a1f">IWMDMStorageGlobals::GetTotalFree</a>
 

 

