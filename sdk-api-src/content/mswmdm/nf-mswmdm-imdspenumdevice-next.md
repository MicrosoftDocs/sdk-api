---
UID: NF:mswmdm.IMDSPEnumDevice.Next
title: IMDSPEnumDevice::Next (mswmdm.h)
description: The Next method retrieves a pointer to the next celtIMDSPDevice interfaces.
helpviewer_keywords: ["IMDSPEnumDevice interface [windows Media Device Manager]","Next method","IMDSPEnumDevice.Next","IMDSPEnumDevice::Next","IMDSPEnumDeviceNext","Next","Next method [windows Media Device Manager]","Next method [windows Media Device Manager]","IMDSPEnumDevice interface","mswmdm/IMDSPEnumDevice::Next","wmdm.imdspenumdevice_next"]
old-location: wmdm\imdspenumdevice_next.htm
tech.root: WMDM
ms.assetid: 137bcc3b-8c6e-4512-b564-a32af437f69a
ms.date: 12/05/2018
ms.keywords: IMDSPEnumDevice interface [windows Media Device Manager],Next method, IMDSPEnumDevice.Next, IMDSPEnumDevice::Next, IMDSPEnumDeviceNext, Next, Next method [windows Media Device Manager], Next method [windows Media Device Manager],IMDSPEnumDevice interface, mswmdm/IMDSPEnumDevice::Next, wmdm.imdspenumdevice_next
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
 - IMDSPEnumDevice::Next
 - mswmdm/IMDSPEnumDevice::Next
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
 - IMDSPEnumDevice.Next
---

# IMDSPEnumDevice::Next


## -description

The <b>Next</b> method retrieves a pointer to the next <i>celt</i><a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice</a> interfaces.

## -parameters

### -param celt [in]

Number of devices requested.

### -param ppDevice [out]

Array of <i>celt</i> pointers <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice</a> allocated by the caller. Return <b>NULL</b> to indicate that no more devices exist or an error has occurred. If <i>celt</i> is more than 1, the caller must allocate enough memory to store <i>celt</i> number of interface pointers.

### -param pceltFetched [out]

Pointer to a <b>ULONG</b> variable that receives the number of interfaces retrieved.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

When there are no more service provider interfaces for enumerated devices, or when there are fewer of these interfaces than requested by the <i>celt</i> parameter, the return value from <b>Next</b> is S_FALSE. When this happens, the <i>pceltFetched</i> parameter must be queried to determine how many interfaces, if any, were returned.

The device enumerator may not reflect the effect of device insertion and removal.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice">IMDSPEnumDevice Interface</a>