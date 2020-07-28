---
UID: NF:vds.IVdsVdProvider.QueryVDisks
title: IVdsVdProvider::QueryVDisks (vds.h)
description: Returns a list of all virtual disks that are managed by the provider.
helpviewer_keywords: ["IVdsVdProvider interface","QueryVDisks method","IVdsVdProvider.QueryVDisks","IVdsVdProvider::QueryVDisks","QueryVDisks","QueryVDisks method","QueryVDisks method","IVdsVdProvider interface","base.ivdsvdprovider_querysurfaceddisks","vds/IVdsVdProvider::QueryVDisks"]
old-location: base\ivdsvdprovider_querysurfaceddisks.htm
tech.root: base
ms.assetid: eab65da4-eb26-46f5-9978-972fd8dffb41
ms.date: 12/05/2018
ms.keywords: IVdsVdProvider interface,QueryVDisks method, IVdsVdProvider.QueryVDisks, IVdsVdProvider::QueryVDisks, QueryVDisks, QueryVDisks method, QueryVDisks method,IVdsVdProvider interface, base.ivdsvdprovider_querysurfaceddisks, vds/IVdsVdProvider::QueryVDisks
f1_keywords:
- vds/IVdsVdProvider.QueryVDisks
dev_langs:
- c++
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
- IVdsVdProvider.QueryVDisks
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsVdProvider::QueryVDisks


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns a list of all virtual disks that are managed by the provider.


## -parameters




### -param ppEnum [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface pointer that can be used to enumerate the virtual disk objects. For more information, see <a href="https://docs.microsoft.com/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the virtual disk  objects when they are no longer needed by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.
     This parameter is required and cannot be <b>NULL</b>.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
</table>
 




## -remarks



If the virtual disk provider does not manage any virtual disks, this method returns an empty enumeration object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsvdprovider">IVdsVdProvider</a>
 

 

