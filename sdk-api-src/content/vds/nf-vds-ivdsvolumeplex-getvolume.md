---
UID: NF:vds.IVdsVolumePlex.GetVolume
title: IVdsVolumePlex::GetVolume
author: windows-sdk-content
description: Returns the volume to which the current plex is a member.
old-location: base\ivdsvolumeplex_getvolume.htm
old-project: VDS
ms.assetid: ddf6102b-81d4-4604-942e-ffb1c2c4730f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetVolume, GetVolume method [VDS], GetVolume method [VDS],IVdsVolumePlex interface, IVdsVolumePlex interface [VDS],GetVolume method, IVdsVolumePlex.GetVolume, IVdsVolumePlex::GetVolume, base.ivdsvolumeplex_getvolume, vds/IVdsVolumePlex::GetVolume
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsVolumePlex.GetVolume
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVolumePlex::GetVolume


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the volume to which the current plex is a member.


## -parameters




### -param ppVolume [out]

The address of an <a href="https://msdn.microsoft.com/a02ee0a6-ac29-406c-9fc0-4f632d32424f">IVdsVolume</a>interface pointer. The caller must release the pointer.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used.




## -see-also




<a href="https://msdn.microsoft.com/a02ee0a6-ac29-406c-9fc0-4f632d32424f">IVdsVolume</a>



<a href="https://msdn.microsoft.com/91970f8b-2b19-4054-8aa2-28e1ea74b3f6">IVdsVolumePlex</a>
 

 

