---
UID: NF:mswmdm.IMDSPDevice.EnumStorage
title: IMDSPDevice::EnumStorage (mswmdm.h)
description: The EnumStorage method retrieves a pointer to an IMDSPEnumStorage interface of an enumerator object that represents the top-level storage(s) on the device. Top-level storage for a device is the root directory of the storage medium.
helpviewer_keywords: ["EnumStorage","EnumStorage method [windows Media Device Manager]","EnumStorage method [windows Media Device Manager]","IMDSPDevice interface","IMDSPDevice interface [windows Media Device Manager]","EnumStorage method","IMDSPDevice.EnumStorage","IMDSPDevice::EnumStorage","IMDSPDeviceEnumStorage","mswmdm/IMDSPDevice::EnumStorage","wmdm.imdspdevice_enumstorage"]
old-location: wmdm\imdspdevice_enumstorage.htm
tech.root: WMDM
ms.assetid: bbf19979-8e09-476e-9401-443ab5e84866
ms.date: 12/05/2018
ms.keywords: EnumStorage, EnumStorage method [windows Media Device Manager], EnumStorage method [windows Media Device Manager],IMDSPDevice interface, IMDSPDevice interface [windows Media Device Manager],EnumStorage method, IMDSPDevice.EnumStorage, IMDSPDevice::EnumStorage, IMDSPDeviceEnumStorage, mswmdm/IMDSPDevice::EnumStorage, wmdm.imdspdevice_enumstorage
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMDSPDevice::EnumStorage
 - mswmdm/IMDSPDevice::EnumStorage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPDevice.EnumStorage
---

# IMDSPDevice::EnumStorage


## -description

The <b>EnumStorage</b> method retrieves a pointer to an <b>IMDSPEnumStorage</b> interface of an enumerator object that represents the top-level storage(s) on the device. Top-level storage for a device is the root directory of the storage medium.

## -parameters

### -param ppEnumStorage [out]

Pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage">IMDSPEnumStorage</a> object.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice Interface</a>