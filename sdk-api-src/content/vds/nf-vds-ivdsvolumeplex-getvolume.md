---
UID: NF:vds.IVdsVolumePlex.GetVolume
title: IVdsVolumePlex::GetVolume (vds.h)
description: Returns the volume to which the current plex is a member.
helpviewer_keywords: ["GetVolume","GetVolume method [VDS]","GetVolume method [VDS]","IVdsVolumePlex interface","IVdsVolumePlex interface [VDS]","GetVolume method","IVdsVolumePlex.GetVolume","IVdsVolumePlex::GetVolume","base.ivdsvolumeplex_getvolume","vds/IVdsVolumePlex::GetVolume"]
old-location: base\ivdsvolumeplex_getvolume.htm
tech.root: base
ms.assetid: ddf6102b-81d4-4604-942e-ffb1c2c4730f
ms.date: 12/05/2018
ms.keywords: GetVolume, GetVolume method [VDS], GetVolume method [VDS],IVdsVolumePlex interface, IVdsVolumePlex interface [VDS],GetVolume method, IVdsVolumePlex.GetVolume, IVdsVolumePlex::GetVolume, base.ivdsvolumeplex_getvolume, vds/IVdsVolumePlex::GetVolume
f1_keywords:
- vds/IVdsVolumePlex.GetVolume
dev_langs:
- c++
req.header: vds.h
req.include-header: 
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsVolumePlex::GetVolume


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the volume to which the current plex is a member.


## -parameters




### -param ppVolume [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>interface pointer. The caller must release the pointer.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsvolumeplex">IVdsVolumePlex</a>
 

 

