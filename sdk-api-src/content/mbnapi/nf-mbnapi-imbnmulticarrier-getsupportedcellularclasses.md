---
UID: NF:mbnapi.IMbnMultiCarrier.GetSupportedCellularClasses
title: IMbnMultiCarrier::GetSupportedCellularClasses (mbnapi.h)
description: Gets the list of supported cellular classes for a multi-carrier device.
helpviewer_keywords: ["GetSupportedCellularClasses","GetSupportedCellularClasses method [Microsoft Broadband Networks]","GetSupportedCellularClasses method [Microsoft Broadband Networks]","IMbnMultiCarrier interface","IMbnMultiCarrier interface [Microsoft Broadband Networks]","GetSupportedCellularClasses method","IMbnMultiCarrier.GetSupportedCellularClasses","IMbnMultiCarrier::GetSupportedCellularClasses","mbn.imbnmulticarrier_getsupportedcellularclasses","mbnapi/IMbnMultiCarrier::GetSupportedCellularClasses"]
old-location: mbn\imbnmulticarrier_getsupportedcellularclasses.htm
tech.root: mbn
ms.assetid: 80B29D28-9940-4A96-B95A-A9640CE5E929
ms.date: 12/05/2018
ms.keywords: GetSupportedCellularClasses, GetSupportedCellularClasses method [Microsoft Broadband Networks], GetSupportedCellularClasses method [Microsoft Broadband Networks],IMbnMultiCarrier interface, IMbnMultiCarrier interface [Microsoft Broadband Networks],GetSupportedCellularClasses method, IMbnMultiCarrier.GetSupportedCellularClasses, IMbnMultiCarrier::GetSupportedCellularClasses, mbn.imbnmulticarrier_getsupportedcellularclasses, mbnapi/IMbnMultiCarrier::GetSupportedCellularClasses
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
 - IMbnMultiCarrier::GetSupportedCellularClasses
 - mbnapi/IMbnMultiCarrier::GetSupportedCellularClasses
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
 - IMbnMultiCarrier.GetSupportedCellularClasses
---

# IMbnMultiCarrier::GetSupportedCellularClasses


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the list of supported cellular classes for a multi-carrier device.

## -parameters

### -param cellularClasses [out, retval]

Pointer to an array of <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_cellular_class">MBN_CELLULAR_CLASS</a> enumerations that contain the list of supported cellular classes. If this method returns any value other than <b>S_OK</b>, <i>cellularClass</i> is <b>NULL</b>. When <b>GetSupportedCellularClasses</b> returns <b>S_OK</b>, the calling application must free the allocated memory by calling <a href="/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy">SafeArrayDestroy</a>.

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