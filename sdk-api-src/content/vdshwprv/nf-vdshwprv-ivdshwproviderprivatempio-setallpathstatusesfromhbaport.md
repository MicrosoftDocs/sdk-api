---
UID: NF:vdshwprv.IVdsHwProviderPrivateMpio.SetAllPathStatusesFromHbaPort
title: IVdsHwProviderPrivateMpio::SetAllPathStatusesFromHbaPort (vdshwprv.h)

description: Sets the statuses of paths originating from a particular HBA port to a specified status.
old-location: base\ivdshwproviderprivatempio_setallpathstatusesfromhbaport.htm
tech.root: VDS
ms.assetid: 1fc25ca9-7cb4-438c-b9da-4bf93bd18a0c

ms.date: 12/05/2018
ms.keywords: IVdsHwProviderPrivateMpio interface [VDS],SetAllPathStatusesFromHbaPort method, IVdsHwProviderPrivateMpio.SetAllPathStatusesFromHbaPort, IVdsHwProviderPrivateMpio::SetAllPathStatusesFromHbaPort, SetAllPathStatusesFromHbaPort, SetAllPathStatusesFromHbaPort method [VDS], SetAllPathStatusesFromHbaPort method [VDS],IVdsHwProviderPrivateMpio interface, base.ivdshwproviderprivatempio_setallpathstatusesfromhbaport, vdshwprv/IVdsHwProviderPrivateMpio::SetAllPathStatusesFromHbaPort
ms.topic: method
f1_keywords:
- vdshwprv/IVdsHwProviderPrivateMpio.SetAllPathStatusesFromHbaPort
dev_langs:
 - c++
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VdsHwPrv.h
api_name:
- IVdsHwProviderPrivateMpio.SetAllPathStatusesFromHbaPort
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsHwProviderPrivateMpio::SetAllPathStatusesFromHbaPort


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the statuses of paths originating from a particular HBA port to a specified status.


## -parameters




### -param hbaPortProp

The properties of the HBA port from which the paths to be set originate.  The only fields that need to be 
      provided are <b>wwnNode</b> and <b>wwnPort</b>.  The hardware provider 
      must ignore all other fields.


### -param status

The status (enumerated by the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_path_status">VDS_PATH_STATUS</a> enumeration) to set the paths.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The association name was successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_S_STATUSES_INCOMPLETELY_SET</b></b></dt>
<dt>0x00042702L</dt>
</dl>
</td>
<td width="60%">
At least one path's status was not successfully set due to a nonfatal error (for example, the status conflicts with 
        the current load balance policy).

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdshwproviderprivatempio">IVdsHwProviderPrivateMpio</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hbaport_prop">VDS_HBAPORT_PROP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_path_status">VDS_PATH_STATUS</a>
 

 

