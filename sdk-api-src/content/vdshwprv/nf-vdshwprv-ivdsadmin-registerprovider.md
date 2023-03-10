---
UID: NF:vdshwprv.IVdsAdmin.RegisterProvider
title: IVdsAdmin::RegisterProvider (vdshwprv.h)
description: Registers the specified hardware provider with VDS. Hardware providers call this method.
helpviewer_keywords: ["IVdsAdmin interface [VDS]","RegisterProvider method","IVdsAdmin.RegisterProvider","IVdsAdmin::RegisterProvider","RegisterProvider","RegisterProvider method [VDS]","RegisterProvider method [VDS]","IVdsAdmin interface","base.ivdsadmin_registerprovider","vdshwprv/IVdsAdmin::RegisterProvider"]
old-location: base\ivdsadmin_registerprovider.htm
tech.root: base
ms.assetid: bb6e0037-7f44-418d-897c-12bf15224841
ms.date: 12/05/2018
ms.keywords: IVdsAdmin interface [VDS],RegisterProvider method, IVdsAdmin.RegisterProvider, IVdsAdmin::RegisterProvider, RegisterProvider, RegisterProvider method [VDS], RegisterProvider method [VDS],IVdsAdmin interface, base.ivdsadmin_registerprovider, vdshwprv/IVdsAdmin::RegisterProvider
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsAdmin::RegisterProvider
 - vdshwprv/IVdsAdmin::RegisterProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsAdmin.RegisterProvider
---

# IVdsAdmin::RegisterProvider


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Registers 
   the specified hardware provider with VDS. Hardware providers call this method.

## -parameters

### -param providerId [in]

The GUID of the hardware provider.

### -param providerClsid [in]

The COM class identifier (Clsid) of the hardware provider.

### -param pwszName [in]

The name of the hardware provider as  a zero-terminated, human-readable string.

### -param type [in]

The provider types enumerated by <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_provider_type">VDS_PROVIDER_TYPE</a>. 
     Use the <b>VDS_PT_HARDWARE</b> value to register a hardware provider with VDS.

### -param pwszMachineName [in]

The name of the computer on which the hardware provider executes; a null-terminated, human-readable string. 
     Use <b>NULL</b> to reference the current computer.

### -param pwszVersion [in]

The  version of the provider as a zero-terminated, human-readable string.

### -param guidVersionId [in]

The GUID for this version of the provider.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ALREADY_REGISTERED</b></dt>
<dt>0x80042403L</dt>
</dl>
</td>
<td width="60%">
The <i>providerId</i> is already registered. Only one version of a provider can be 
       registered at any given time.

</td>
</tr>
</table>

## -remarks

If necessary, call 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsadmin-unregisterprovider">UnregisterProvider</a> to remove a provider 
    before registering a new version.

An in-process provider calls this method from 
    <a href="/windows/desktop/api/olectl/nf-olectl-dllregisterserver">DllRegisterServer</a>; whereas, an out-of-process 
    provider calls from the 
    <a href="/windows/desktop/api/winbase/nf-winbase-winmain">WinMain</a> 
    function.

Hardware providers must not stop running while VDS is running.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadmin">IVdsAdmin</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsadmin-unregisterprovider">IVdsAdmin::UnregisterProvider</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_provider_type">VDS_PROVIDER_TYPE</a>