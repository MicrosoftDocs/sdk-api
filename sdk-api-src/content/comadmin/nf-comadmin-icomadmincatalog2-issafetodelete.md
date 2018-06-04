---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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




<a href="https://msdn.microsoft.com/ffca611d-dacc-47be-9101-9de76ecc8393">ICOMAdminCatalog2</a>
 

 

