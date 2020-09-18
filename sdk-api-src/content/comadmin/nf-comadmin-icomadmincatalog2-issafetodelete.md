---
UID: NF:comadmin.ICOMAdminCatalog2.IsSafeToDelete
title: ICOMAdminCatalog2::IsSafeToDelete (comadmin.h)
description: Determines whether the specified DLL is in use by the COM+ catalog or the registry.
helpviewer_keywords: ["COMAdminInUseByCatalog","COMAdminInUseByRegistryClsid","COMAdminInUseByRegistryProxyStub","COMAdminInUseByRegistryTypeLib","COMAdminInUseByRegistryUnknown","COMAdminNotInUse","ICOMAdminCatalog2 interface [COM+]","IsSafeToDelete method","ICOMAdminCatalog2.IsSafeToDelete","ICOMAdminCatalog2::IsSafeToDelete","IsSafeToDelete","IsSafeToDelete method [COM+]","IsSafeToDelete method [COM+]","ICOMAdminCatalog2 interface","_cos_icomadmincatalog2_IsSafeToDelete","comadmin/ICOMAdminCatalog2::IsSafeToDelete","cos.icomadmincatalog2_issafetodelete"]
old-location: cos\icomadmincatalog2_issafetodelete.htm
tech.root: cos
ms.assetid: 293644a2-e400-47fc-803d-cf86ba97eb7d
ms.date: 12/05/2018
ms.keywords: COMAdminInUseByCatalog, COMAdminInUseByRegistryClsid, COMAdminInUseByRegistryProxyStub, COMAdminInUseByRegistryTypeLib, COMAdminInUseByRegistryUnknown, COMAdminNotInUse, ICOMAdminCatalog2 interface [COM+],IsSafeToDelete method, ICOMAdminCatalog2.IsSafeToDelete, ICOMAdminCatalog2::IsSafeToDelete, IsSafeToDelete, IsSafeToDelete method [COM+], IsSafeToDelete method [COM+],ICOMAdminCatalog2 interface, _cos_icomadmincatalog2_IsSafeToDelete, comadmin/ICOMAdminCatalog2::IsSafeToDelete, cos.icomadmincatalog2_issafetodelete
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
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
 - ICOMAdminCatalog2::IsSafeToDelete
 - comadmin/ICOMAdminCatalog2::IsSafeToDelete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog2.IsSafeToDelete
---

# ICOMAdminCatalog2::IsSafeToDelete


## -description

Determines whether the specified DLL is in use by the COM+ catalog or the registry.

## -parameters

### -param bstrDllName [in]

The full path to the DLL to be tested.

### -param pCOMAdminInUse [out, retval]

Indicates the DLL usage. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="COMAdminNotInUse"></a><a id="comadminnotinuse"></a><a id="COMADMINNOTINUSE"></a><dl>
<dt><b>COMAdminNotInUse</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The DLL is not in use and may safely be deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminInUseByCatalog"></a><a id="comadmininusebycatalog"></a><a id="COMADMININUSEBYCATALOG"></a><dl>
<dt><b>COMAdminInUseByCatalog</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The DLL is in use by the COM+ catalog.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminInUseByRegistryUnknown"></a><a id="comadmininusebyregistryunknown"></a><a id="COMADMININUSEBYREGISTRYUNKNOWN"></a><dl>
<dt><b>COMAdminInUseByRegistryUnknown</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The DLL is in use by an unknown registry component.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminInUseByRegistryProxyStub"></a><a id="comadmininusebyregistryproxystub"></a><a id="COMADMININUSEBYREGISTRYPROXYSTUB"></a><dl>
<dt><b>COMAdminInUseByRegistryProxyStub</b></dt>
<dt>0x3</dt>
</dl>
</td>
<td width="60%">
The DLL is in use by the proxy registry component.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminInUseByRegistryTypeLib"></a><a id="comadmininusebyregistrytypelib"></a><a id="COMADMININUSEBYREGISTRYTYPELIB"></a><dl>
<dt><b>COMAdminInUseByRegistryTypeLib</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The DLL is in use by the TypeLib registry component.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminInUseByRegistryClsid"></a><a id="comadmininusebyregistryclsid"></a><a id="COMADMININUSEBYREGISTRYCLSID"></a><dl>
<dt><b>COMAdminInUseByRegistryClsid</b></dt>
<dt>0x5</dt>
</dl>
</td>
<td width="60%">
The DLL is in use by the CLSID registry component.

</td>
</tr>
</table>

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>