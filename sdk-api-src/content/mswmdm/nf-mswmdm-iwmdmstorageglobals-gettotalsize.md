---
UID: NF:mswmdm.IWMDMStorageGlobals.GetTotalSize
title: IWMDMStorageGlobals::GetTotalSize (mswmdm.h)
author: windows-sdk-content
description: The GetTotalSize method retrieves the total size in bytes of the storage medium associated with the IWMDMStorageGlobals interface.
old-location: wmdm\iwmdmstorageglobals_gettotalsize.htm
tech.root: WMDM
ms.assetid: ebbc8b7e-037f-4b8d-b026-793d38914685
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTotalSize, GetTotalSize method [windows Media Device Manager], GetTotalSize method [windows Media Device Manager],IWMDMStorageGlobals interface, IWMDMStorageGlobals interface [windows Media Device Manager],GetTotalSize method, IWMDMStorageGlobals.GetTotalSize, IWMDMStorageGlobals::GetTotalSize, IWMDMStorageGlobalsGetTotalSize, mswmdm/IWMDMStorageGlobals::GetTotalSize, wmdm.iwmdmstorageglobals_gettotalsize
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
 - IWMDMStorageGlobals.GetTotalSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMStorageGlobals::GetTotalSize


## -description



The <b>GetTotalSize</b> method retrieves the total size in bytes of the storage medium associated with the <b>IWMDMStorageGlobals</b> interface.




## -parameters




### -param pdwTotalSizeLow [out]

Pointer to a <b>DWORD</b> that receives the low-order value of the total size of the medium.


### -param pdwTotalSizeHigh [out]

Pointer to a <b>DWORD</b> that receives the high-order value of the total size of the medium.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/fe164271-58f0-4b28-a200-6b15f8b42d36">IWMDMStorageGlobals Interface</a>



<a href="https://msdn.microsoft.com/a97c2d92-dc54-4987-b2b4-e4de2e546a1f">IWMDMStorageGlobals::GetTotalFree</a>
 

 

