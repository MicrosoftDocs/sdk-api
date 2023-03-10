---
UID: NF:ehstorapi.IEnhancedStorageSilo.GetPortableDevice
title: IEnhancedStorageSilo::GetPortableDevice (ehstorapi.h)
description: Obtains an IPortableDevice pointer used to issue commands to the corresponding Enhanced Storage silo driver.
helpviewer_keywords: ["GetPortableDevice","GetPortableDevice method [Enhanced Storage]","GetPortableDevice method [Enhanced Storage]","IEnhancedStorageSilo interface","IEnhancedStorageSilo interface [Enhanced Storage]","GetPortableDevice method","IEnhancedStorageSilo.GetPortableDevice","IEnhancedStorageSilo::GetPortableDevice","ehstorapi/IEnhancedStorageSilo::GetPortableDevice","enstor.ienhancedstoragesilo_getportabledevice"]
old-location: enstor\ienhancedstoragesilo_getportabledevice.htm
tech.root: enstor
ms.assetid: a95323d1-4329-4a1e-9c8a-adfdd199e9a5
ms.date: 12/05/2018
ms.keywords: GetPortableDevice, GetPortableDevice method [Enhanced Storage], GetPortableDevice method [Enhanced Storage],IEnhancedStorageSilo interface, IEnhancedStorageSilo interface [Enhanced Storage],GetPortableDevice method, IEnhancedStorageSilo.GetPortableDevice, IEnhancedStorageSilo::GetPortableDevice, ehstorapi/IEnhancedStorageSilo::GetPortableDevice, enstor.ienhancedstoragesilo_getportabledevice
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
 - IEnhancedStorageSilo::GetPortableDevice
 - ehstorapi/IEnhancedStorageSilo::GetPortableDevice
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
 - IEnhancedStorageSilo.GetPortableDevice
---

# IEnhancedStorageSilo::GetPortableDevice


## -description

Obtains an <a href="/windows/win32/api/portabledeviceapi/nn-portabledeviceapi-iportabledevice">IPortableDevice</a> pointer used to issue  commands to the corresponding Enhanced Storage silo driver.

## -parameters

### -param ppIPortableDevice [out]

Pointer to a pointer to an <a href="/windows/win32/api/portabledeviceapi/nn-portabledeviceapi-iportabledevice">IPortableDevice</a>  object.

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
Pointer to <a href="/windows/win32/api/portabledeviceapi/nn-portabledeviceapi-iportabledevice">IPortableDevice</a> was obtained successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppIPortableDevice</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesilo">IEnhancedStorageSilo</a>