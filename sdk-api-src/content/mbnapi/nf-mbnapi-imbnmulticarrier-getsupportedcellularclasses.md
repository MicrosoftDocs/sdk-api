---
UID: NF:mbnapi.IMbnMultiCarrier.GetSupportedCellularClasses
title: IMbnMultiCarrier::GetSupportedCellularClasses
author: windows-sdk-content
description: Gets the list of supported cellular classes for a multi-carrier device.
old-location: mbn\imbnmulticarrier_getsupportedcellularclasses.htm
tech.root: mbn
ms.assetid: 80B29D28-9940-4A96-B95A-A9640CE5E929
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetSupportedCellularClasses, GetSupportedCellularClasses method [Microsoft Broadband Networks], GetSupportedCellularClasses method [Microsoft Broadband Networks],IMbnMultiCarrier interface, IMbnMultiCarrier interface [Microsoft Broadband Networks],GetSupportedCellularClasses method, IMbnMultiCarrier.GetSupportedCellularClasses, IMbnMultiCarrier::GetSupportedCellularClasses, mbn.imbnmulticarrier_getsupportedcellularclasses, mbnapi/IMbnMultiCarrier::GetSupportedCellularClasses
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnMultiCarrier.GetSupportedCellularClasses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnMultiCarrier::GetSupportedCellularClasses


## -description


Gets the list of supported cellular classes for a multi-carrier device.


## -parameters




### -param cellularClasses

TBD




#### - cellularClass [out, retval]

Pointer to an array of <a href="https://msdn.microsoft.com/2d75c20b-1ae4-4824-8918-41c20327a007">MBN_CELLULAR_CLASS</a> enumerations that contain the list of supported cellular classes. If this method returns any value other than <b>S_OK</b>, <i>cellularClass</i> is <b>NULL</b>. When <b>GetSupportedCellularClasses</b> returns <b>S_OK</b>, the calling application must free the allocated memory by calling <a href="https://msdn.microsoft.com/fc94f7e7-b903-4c78-905c-54df1f8d13fa">SafeArrayDestroy</a>.


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




<a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a>
 

 

