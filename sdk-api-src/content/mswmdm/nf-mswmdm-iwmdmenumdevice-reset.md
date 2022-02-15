---
UID: NF:mswmdm.IWMDMEnumDevice.Reset
title: IWMDMEnumDevice::Reset (mswmdm.h)
description: The Reset method resets the enumeration so that Next returns a pointer to the first device.
helpviewer_keywords: ["IWMDMEnumDevice interface [windows Media Device Manager]","Reset method","IWMDMEnumDevice.Reset","IWMDMEnumDevice::Reset","IWMDMEnumDeviceReset","Reset","Reset method [windows Media Device Manager]","Reset method [windows Media Device Manager]","IWMDMEnumDevice interface","mswmdm/IWMDMEnumDevice::Reset","wmdm.iwmdmenumdevice_reset"]
old-location: wmdm\iwmdmenumdevice_reset.htm
tech.root: WMDM
ms.assetid: af06bc07-2043-4ef5-a1f2-381797fb750b
ms.date: 12/05/2018
ms.keywords: IWMDMEnumDevice interface [windows Media Device Manager],Reset method, IWMDMEnumDevice.Reset, IWMDMEnumDevice::Reset, IWMDMEnumDeviceReset, Reset, Reset method [windows Media Device Manager], Reset method [windows Media Device Manager],IWMDMEnumDevice interface, mswmdm/IWMDMEnumDevice::Reset, wmdm.iwmdmenumdevice_reset
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
 - IWMDMEnumDevice::Reset
 - mswmdm/IWMDMEnumDevice::Reset
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
 - IWMDMEnumDevice.Reset
---

# IWMDMEnumDevice::Reset


## -description

The <b>Reset</b> method resets the enumeration so that <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next">Next</a> returns a pointer to the first device.



## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice">IWMDMEnumDevice Interface</a>
