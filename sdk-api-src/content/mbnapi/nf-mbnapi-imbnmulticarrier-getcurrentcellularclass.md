---
UID: NF:mbnapi.IMbnMultiCarrier.GetCurrentCellularClass
title: IMbnMultiCarrier::GetCurrentCellularClass
author: windows-sdk-content
description: Gets the current cellular classes for a multi-carrier device.
old-location: mbn\imbnmulticarrier_getcurrentcellularclass.htm
old-project: mbn
ms.assetid: 8DA29C25-3866-4BCA-8591-F8408A1C1401
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetCurrentCellularClass, GetCurrentCellularClass method [Microsoft Broadband Networks], GetCurrentCellularClass method [Microsoft Broadband Networks],IMbnMultiCarrier interface, IMbnMultiCarrier interface [Microsoft Broadband Networks],GetCurrentCellularClass method, IMbnMultiCarrier.GetCurrentCellularClass, IMbnMultiCarrier::GetCurrentCellularClass, mbn.imbnmulticarrier_getcurrentcellularclass, mbnapi/IMbnMultiCarrier::GetCurrentCellularClass
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnMultiCarrier.GetCurrentCellularClass
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnMultiCarrier::GetCurrentCellularClass


## -description


Gets the current cellular classes for a multi-carrier device.


## -parameters




### -param currentCellularClass [out, retval]


<a href="https://msdn.microsoft.com/2d75c20b-1ae4-4824-8918-41c20327a007">MBN_CELLULAR_CLASS</a>


Pointer to an <a href="https://msdn.microsoft.com/2d75c20b-1ae4-4824-8918-41c20327a007">MBN_CELLULAR_CLASS</a> enumeration that specifies the current cellular class. If this method returns any value other than <b>S_OK</b>, <i>currentCellularClass</i> is <b>NULL</b>. When <b>GetCurrentCellularClass</b> returns <b>S_OK</b>, the calling application must free the allocated memory by calling <a href="https://msdn.microsoft.com/fc94f7e7-b903-4c78-905c-54df1f8d13fa">SafeArrayDestroy</a>.


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
 

 

