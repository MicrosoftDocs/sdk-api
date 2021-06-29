---
UID: NF:mswmdm.IMDSPEnumDevice.Reset
title: IMDSPEnumDevice::Reset (mswmdm.h)
description: The Reset method resets the enumeration sequence to the beginning. A subsequent call to Next fetches the first Windows Media Device Manager interface in the enumeration sequence.
helpviewer_keywords: ["IMDSPEnumDevice interface [windows Media Device Manager]","Reset method","IMDSPEnumDevice.Reset","IMDSPEnumDevice::Reset","IMDSPEnumDeviceReset","Reset","Reset method [windows Media Device Manager]","Reset method [windows Media Device Manager]","IMDSPEnumDevice interface","mswmdm/IMDSPEnumDevice::Reset","wmdm.imdspenumdevice_reset"]
old-location: wmdm\imdspenumdevice_reset.htm
tech.root: WMDM
ms.assetid: 7edd0d45-aeae-4bc8-b4d4-f74bcb403ef9
ms.date: 12/05/2018
ms.keywords: IMDSPEnumDevice interface [windows Media Device Manager],Reset method, IMDSPEnumDevice.Reset, IMDSPEnumDevice::Reset, IMDSPEnumDeviceReset, Reset, Reset method [windows Media Device Manager], Reset method [windows Media Device Manager],IMDSPEnumDevice interface, mswmdm/IMDSPEnumDevice::Reset, wmdm.imdspenumdevice_reset
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
 - IMDSPEnumDevice::Reset
 - mswmdm/IMDSPEnumDevice::Reset
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
 - IMDSPEnumDevice.Reset
---

# IMDSPEnumDevice::Reset


## -description

The <b>Reset</b> method resets the enumeration sequence to the beginning. A subsequent call to <b>Next</b> fetches the first Windows Media Device Manager interface in the enumeration sequence.



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

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice">IMDSPEnumDevice Interface</a>
