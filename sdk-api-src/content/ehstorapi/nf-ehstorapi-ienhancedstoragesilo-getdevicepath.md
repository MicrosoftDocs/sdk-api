---
UID: NF:ehstorapi.IEnhancedStorageSilo.GetDevicePath
title: IEnhancedStorageSilo::GetDevicePath (ehstorapi.h)
description: Retrieves the path to the silo device node. The returned string is suitable for passing to Windows System APIs such as CreateFile or SetupDiOpenDeviceInterface.
helpviewer_keywords: ["GetDevicePath","GetDevicePath method [Enhanced Storage]","GetDevicePath method [Enhanced Storage]","IEnhancedStorageSilo interface","IEnhancedStorageSilo interface [Enhanced Storage]","GetDevicePath method","IEnhancedStorageSilo.GetDevicePath","IEnhancedStorageSilo::GetDevicePath","ehstorapi/IEnhancedStorageSilo::GetDevicePath","enstor.ienhancedstoragesilo_getdevicepath"]
old-location: enstor\ienhancedstoragesilo_getdevicepath.htm
tech.root: enstor
ms.assetid: 98ef04a1-d14d-4de3-b24a-0f044335d75b
ms.date: 12/05/2018
ms.keywords: GetDevicePath, GetDevicePath method [Enhanced Storage], GetDevicePath method [Enhanced Storage],IEnhancedStorageSilo interface, IEnhancedStorageSilo interface [Enhanced Storage],GetDevicePath method, IEnhancedStorageSilo.GetDevicePath, IEnhancedStorageSilo::GetDevicePath, ehstorapi/IEnhancedStorageSilo::GetDevicePath, enstor.ienhancedstoragesilo_getdevicepath
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EhStorAPI.idl
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
 - IEnhancedStorageSilo::GetDevicePath
 - ehstorapi/IEnhancedStorageSilo::GetDevicePath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EhStorAPI.h
api_name:
 - IEnhancedStorageSilo.GetDevicePath
---

# IEnhancedStorageSilo::GetDevicePath


## -description

Retrieves the path to the silo device node. The returned string is suitable for passing to <b>Windows System</b> APIs such as <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> or <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea">SetupDiOpenDeviceInterface</a>.

## -parameters

### -param ppwszSiloDevicePath [out]

A pointer to a string that represents the path to the Silo device node.

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
Device path string was retrieved successfully. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppwszSiloDevicePath</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The memory to contain the device path string is allocated by the Enhanced Storage API and must be freed  by passing the  returned pointer to <a href="/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesilo">IEnhancedStorageSilo</a>