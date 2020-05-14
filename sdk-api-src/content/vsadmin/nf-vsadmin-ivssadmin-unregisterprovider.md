---
UID: NF:vsadmin.IVssAdmin.UnregisterProvider
title: IVssAdmin::UnregisterProvider (vsadmin.h)
description: Unregisters an existing provider.helpviewer_keywords: ["IVssAdmin interface [VSS]","UnregisterProvider method","IVssAdmin.UnregisterProvider","IVssAdmin::UnregisterProvider","UnregisterProvider","UnregisterProvider method [VSS]","UnregisterProvider method [VSS]","IVssAdmin interface","base.ivssadmin_unregisterprovider","vsadmin/IVssAdmin::UnregisterProvider"]
old-location: base\ivssadmin_unregisterprovider.htm
tech.root: VSS
ms.assetid: d31ed47f-6850-4f4b-aea2-5171722db7db
ms.date: 12/05/2018
ms.keywords: IVssAdmin interface [VSS],UnregisterProvider method, IVssAdmin.UnregisterProvider, IVssAdmin::UnregisterProvider, UnregisterProvider, UnregisterProvider method [VSS], UnregisterProvider method [VSS],IVssAdmin interface, base.ivssadmin_unregisterprovider, vsadmin/IVssAdmin::UnregisterProvider
f1_keywords:
- vsadmin/IVssAdmin.UnregisterProvider
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VsAdmin.h
api_name:
- IVssAdmin.UnregisterProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssAdmin::UnregisterProvider


## -description


The <b>UnregisterProvider</b> 
   method unregisters an existing provider.


## -parameters




### -param ProviderId [in]

The <b>VSS_ID</b> of the provider. 


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The provider was unregistered successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VSS_E_PROVIDER_IN_USE</b></b></dt>
</dl>
</td>
<td width="60%">
The provider is in use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VSS_E_PROVIDER_NOT_REGISTERED</b></b></dt>
</dl>
</td>
<td width="60%">
The provider is not registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_OUTOFMEMORY</b></b></dt>
</dl>
</td>
<td width="60%">
Out of memory or other system resources.

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
        <a href="https://docs.microsoft.com/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vsadmin/nn-vsadmin-ivssadmin">IVssAdmin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsadmin/nf-vsadmin-ivssadmin-registerprovider">RegisterProvider</a>
 

 

