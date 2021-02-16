---
UID: NF:mbnapi.IMbnMultiCarrier.GetCurrentCellularClass
title: IMbnMultiCarrier::GetCurrentCellularClass (mbnapi.h)
description: Gets the current cellular classes for a multi-carrier device.
helpviewer_keywords: ["GetCurrentCellularClass","GetCurrentCellularClass method [Microsoft Broadband Networks]","GetCurrentCellularClass method [Microsoft Broadband Networks]","IMbnMultiCarrier interface","IMbnMultiCarrier interface [Microsoft Broadband Networks]","GetCurrentCellularClass method","IMbnMultiCarrier.GetCurrentCellularClass","IMbnMultiCarrier::GetCurrentCellularClass","mbn.imbnmulticarrier_getcurrentcellularclass","mbnapi/IMbnMultiCarrier::GetCurrentCellularClass"]
old-location: mbn\imbnmulticarrier_getcurrentcellularclass.htm
tech.root: mbn
ms.assetid: 8DA29C25-3866-4BCA-8591-F8408A1C1401
ms.date: 12/05/2018
ms.keywords: GetCurrentCellularClass, GetCurrentCellularClass method [Microsoft Broadband Networks], GetCurrentCellularClass method [Microsoft Broadband Networks],IMbnMultiCarrier interface, IMbnMultiCarrier interface [Microsoft Broadband Networks],GetCurrentCellularClass method, IMbnMultiCarrier.GetCurrentCellularClass, IMbnMultiCarrier::GetCurrentCellularClass, mbn.imbnmulticarrier_getcurrentcellularclass, mbnapi/IMbnMultiCarrier::GetCurrentCellularClass
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - IMbnMultiCarrier::GetCurrentCellularClass
 - mbnapi/IMbnMultiCarrier::GetCurrentCellularClass
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnMultiCarrier.GetCurrentCellularClass
---

# IMbnMultiCarrier::GetCurrentCellularClass


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the current cellular classes for a multi-carrier device.

## -parameters

### -param currentCellularClass [out, retval]

<a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_cellular_class">MBN_CELLULAR_CLASS</a>


Pointer to an <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_cellular_class">MBN_CELLULAR_CLASS</a> enumeration that specifies the current cellular class. If this method returns any value other than <b>S_OK</b>, <i>currentCellularClass</i> is <b>NULL</b>. When <b>GetCurrentCellularClass</b> returns <b>S_OK</b>, the calling application must free the allocated memory by calling <a href="/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy">SafeArrayDestroy</a>.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_SERVICE_NOT_ACTIVE)</b></dt>
</dl>
</td>
<td width="60%">
The Mobile Broadband service is not running on this system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface.  The Mobile Broadband device has probably been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface.  Most likely the Mobile Broadband device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported by the device. This may be returned by devices which do not support multi-carrier.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrier">IMbnMultiCarrier</a>