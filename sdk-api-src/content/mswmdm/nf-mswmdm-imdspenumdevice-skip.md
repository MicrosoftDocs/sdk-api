---
UID: NF:mswmdm.IMDSPEnumDevice.Skip
title: IMDSPEnumDevice::Skip (mswmdm.h)
description: The Skip method skips over the next specified number of media device interface(s) in the enumeration sequence.
helpviewer_keywords: ["IMDSPEnumDevice interface [windows Media Device Manager]","Skip method","IMDSPEnumDevice.Skip","IMDSPEnumDevice::Skip","IMDSPEnumDeviceSkip","Skip","Skip method [windows Media Device Manager]","Skip method [windows Media Device Manager]","IMDSPEnumDevice interface","mswmdm/IMDSPEnumDevice::Skip","wmdm.imdspenumdevice_skip"]
old-location: wmdm\imdspenumdevice_skip.htm
tech.root: WMDM
ms.assetid: 17b4e680-7f55-4f96-a0ca-acfda9f17784
ms.date: 12/05/2018
ms.keywords: IMDSPEnumDevice interface [windows Media Device Manager],Skip method, IMDSPEnumDevice.Skip, IMDSPEnumDevice::Skip, IMDSPEnumDeviceSkip, Skip, Skip method [windows Media Device Manager], Skip method [windows Media Device Manager],IMDSPEnumDevice interface, mswmdm/IMDSPEnumDevice::Skip, wmdm.imdspenumdevice_skip
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
 - IMDSPEnumDevice::Skip
 - mswmdm/IMDSPEnumDevice::Skip
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
 - IMDSPEnumDevice.Skip
---

# IMDSPEnumDevice::Skip


## -description

The <b>Skip</b> method skips over the next specified number of media device interface(s) in the enumeration sequence.

## -parameters

### -param celt [in]

Number of elements to skip.

### -param pceltFetched [out]

Pointer to the number of elements that actually were skipped.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

If the number specified in the <i>celt</i> parameter is greater than the actual number of interfaces remaining in the enumeration sequence, then the return value from <b>Skip</b> is S_FALSE. When this happens, the <i>pceltFetched</i> parameter must be queried to determine how many interfaces were skipped. If you skip to the end of the array of enumerated media device interfaces, a subsequent call to <b>Next</b> returns S_FALSE.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice">IMDSPEnumDevice Interface</a>