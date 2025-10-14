---
UID: NF:vsadmin.IVssAdmin.RegisterProvider
title: IVssAdmin::RegisterProvider (vsadmin.h)
description: Registers a new shadow copy provider.
helpviewer_keywords: ["IVssAdmin interface [VSS]","RegisterProvider method","IVssAdmin.RegisterProvider","IVssAdmin::RegisterProvider","RegisterProvider","RegisterProvider method [VSS]","RegisterProvider method [VSS]","IVssAdmin interface","base.ivssadmin_registerprovider","vsadmin/IVssAdmin::RegisterProvider"]
old-location: base\ivssadmin_registerprovider.htm
tech.root: base
ms.assetid: c17aee22-3afc-4ac5-a0c5-3fa1164ceee0
ms.date: 12/05/2018
ms.keywords: IVssAdmin interface [VSS],RegisterProvider method, IVssAdmin.RegisterProvider, IVssAdmin::RegisterProvider, RegisterProvider, RegisterProvider method [VSS], RegisterProvider method [VSS],IVssAdmin interface, base.ivssadmin_registerprovider, vsadmin/IVssAdmin::RegisterProvider
req.header: vsadmin.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssAdmin::RegisterProvider
 - vsadmin/IVssAdmin::RegisterProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsAdmin.h
api_name:
 - IVssAdmin.RegisterProvider
---

# IVssAdmin::RegisterProvider


## -description

The <b>RegisterProvider</b> method 
  registers a new shadow copy provider.

## -parameters

### -param pProviderId [in]

The <b>VSS_ID</b> that uniquely and persistently identifies the provider. After it is 
     defined, the <i>ProviderId</i> parameter should remain the same, even when the software 
     revision is updated. A <i>ProviderId</i> parameter should be changed only when the 
     functionality changes enough that both providers would be active on the same system. A requester may use the 
     <i>ProviderId</i> parameter to request that a specific provider be used in a shadow copy 
     creation.

### -param ClassId [in]

The CLSID of the provider.

### -param pwszProviderName [in]

The name of the provider.

### -param eProviderType [in]

A 
     <a href="/windows/desktop/api/vss/ne-vss-vss_provider_type">VSS_PROVIDER_TYPE</a> enumeration value that specifies the provider type. Note that <b>VSS_PROV_HARDWARE</b> is not a valid provider type on Windows client operating system versions. Hardware providers will run only on Windows server operating system versions.

### -param pwszProviderVersion [in]

The version of the provider.

### -param ProviderVersionId [in]

The <b>VSS_ID</b> that uniquely identifies this version of the  provider. The 
     combination of the <i>pProviderId</i> and <i>ProviderVersionId</i> 
     parameters should be unique. The  <i>ProviderVersionId</i> parameter can be the same as the 
     <i>ProviderVersionId</i> parameter of another provider.

## -returns

This method can return one of these values.

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
The provider was registered successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameter values is not valid. For example, <b>VSS_PROV_HARDWARE</b> is not a valid provider type on Windows client operating system versions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_ALREADY_REGISTERED</b></dt>
</dl>
</td>
<td width="60%">
The provider has already been registered on this computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>

## -remarks

If the hardware provider is updated, the setup application should call the 
   <a href="/windows/desktop/api/vsadmin/nf-vsadmin-ivssadmin-unregisterprovider">UnregisterProvider</a> method to unregister the 
   outdated version, and then call  the 
   <b>RegisterProvider</b> method to register the 
   updated provider.

<div class="alert"><b>Note</b>  Hardware providers can only be registered on Windows Server operating systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vsadmin/nn-vsadmin-ivssadmin">IVssAdmin</a>



<a href="/windows/desktop/api/vsadmin/nf-vsadmin-ivssadmin-unregisterprovider">UnregisterProvider</a>