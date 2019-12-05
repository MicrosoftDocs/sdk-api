---
UID: NF:vdshwprv.IVdsLun.QueryPlexes
title: IVdsLun::QueryPlexes (vdshwprv.h)
description: Returns an enumeration of the plexes in a LUN.
old-location: base\ivdslun_queryplexes.htm
tech.root: VDS
ms.assetid: 128708cb-2ad1-45be-8e38-b5fd943d0945
ms.date: 12/05/2018
ms.keywords: IVdsLun interface [VDS],QueryPlexes method, IVdsLun.QueryPlexes, IVdsLun::QueryPlexes, QueryPlexes, QueryPlexes method [VDS], QueryPlexes method [VDS],IVdsLun interface, base.ivdslun_queryplexes, vds/IVdsLun::QueryPlexes, vdshwprv/IVdsLun::QueryPlexes
ms.topic: method
f1_keywords:
- vdshwprv/IVdsLun.QueryPlexes
dev_langs:
- c++
req.header: vdshwprv.h
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
- IVdsLun.QueryPlexes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsLun::QueryPlexes


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an 
   enumeration of the plexes in a LUN.


## -parameters




### -param ppEnum [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface 
      pointer that can be used to enumerate the plexes  as <a href="https://docs.microsoft.com/windows/desktop/VDS/lun-plex-object">LUN plex objects</a>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the LUN  plex objects when they are no longer needed by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.




## -remarks



All LUNs must have at least one plex; mirrored LUNs have multiple plexes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a>
 

 

