---
UID: NF:vds.IVdsDrive2.GetProperties2
title: IVdsDrive2::GetProperties2
author: windows-sdk-content
description: Returns the properties of a drive object.
old-location: base\ivdsdrive2_getproperties2.htm
old-project: VDS
ms.assetid: 635957be-780f-4dee-8d70-b7fc37fecd5c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: GetProperties2, GetProperties2 method, GetProperties2 method,IVdsDrive2 interface, IVdsDrive2 interface,GetProperties2 method, IVdsDrive2.GetProperties2, IVdsDrive2::GetProperties2, base.ivdsdrive2_getproperties2, vds/IVdsDrive2::GetProperties2, vdshwprv/IVdsDrive2::GetProperties2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - IVdsDrive2.GetProperties2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsDrive2::GetProperties2


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the properties of a drive object.


## -parameters




### -param pDriveProp2 [out]

The address of the <a href="https://msdn.microsoft.com/af932865-abb3-4dee-a7dc-3aa06fd167f6">VDS_DRIVE_PROP2</a> structure 
      allocated and passed in by the caller. VDS allocates memory for the 
      <b>pwszFriendlyName</b> and <b>pwszIdentification</b> member strings. 
      Callers must free the strings by using the 
      <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function. This parameter is required and cannot be <b>NULL</b>.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used.




## -remarks



This method must return zero (S_OK) to indicate success, or an implementation-specific nonzero error code to indicate failure.




## -see-also




<a href="https://msdn.microsoft.com/6d8115e3-2a47-4bc3-9a69-24e26f555f41">IVdsDrive2</a>
 

 

