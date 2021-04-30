---
UID: NF:mswmdm.IWMDMEnumDevice.Clone
title: IWMDMEnumDevice::Clone (mswmdm.h)
description: The Clone method returns a copy of the IWMDMEnumDevice interface. The new enumerator specifies the same enumeration state as the current enumerator.
helpviewer_keywords: ["Clone","Clone method [windows Media Device Manager]","Clone method [windows Media Device Manager]","IWMDMEnumDevice interface","IWMDMEnumDevice interface [windows Media Device Manager]","Clone method","IWMDMEnumDevice.Clone","IWMDMEnumDevice::Clone","IWMDMEnumDeviceClone","mswmdm/IWMDMEnumDevice::Clone","wmdm.iwmdmenumdevice_clone"]
old-location: wmdm\iwmdmenumdevice_clone.htm
tech.root: WMDM
ms.assetid: c8118950-d96f-4720-ab3a-f5ea93065875
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [windows Media Device Manager], Clone method [windows Media Device Manager],IWMDMEnumDevice interface, IWMDMEnumDevice interface [windows Media Device Manager],Clone method, IWMDMEnumDevice.Clone, IWMDMEnumDevice::Clone, IWMDMEnumDeviceClone, mswmdm/IWMDMEnumDevice::Clone, wmdm.iwmdmenumdevice_clone
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
 - IWMDMEnumDevice::Clone
 - mswmdm/IWMDMEnumDevice::Clone
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
 - IWMDMEnumDevice.Clone
---

# IWMDMEnumDevice::Clone


## -description

The <b>Clone</b> method returns a copy of the <b>IWMDMEnumDevice</b> interface. The new enumerator specifies the same enumeration state as the current enumerator.

## -parameters

### -param ppEnumDevice [out]

Address of a pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice">IWMDMEnumDevice</a> interface. The caller must release this interface when done with it.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Using this method, a client can record a particular point in the enumeration sequence and return to that point later. The new enumerator supports the same interface as the original one.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice">IWMDMEnumDevice Interface</a>