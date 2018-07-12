---
UID: NF:setupapi.SetupDiGetDriverInfoDetailW
title: SetupDiGetDriverInfoDetailW function
author: windows-sdk-content
description: The SetupDiGetDriverInfoDetail function retrieves driver information detail for a device information set or a particular device information element in the device information set.
old-location: devinst\setupdigetdriverinfodetail.htm
old-project: devinst
ms.assetid: 42f3668c-8112-4cc0-bce8-b0b3886c45fb
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: SetupDiGetDriverInfoDetail, SetupDiGetDriverInfoDetail function [Device and Driver Installation], SetupDiGetDriverInfoDetailA, SetupDiGetDriverInfoDetailW, devinst.setupdigetdriverinfodetail, di-rtns_5a2fb98d-54ee-4290-9969-f5e12d77cbcf.xml, setupapi/SetupDiGetDriverInfoDetail
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetDriverInfoDetail
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# SetupDiGetDriverInfoDetailW function


## -description


The <b>SetupDiGetDriverInfoDetail</b> function retrieves driver information detail for a device information set or a particular device information element in the device information set.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> that contains a driver information element for which to retrieve driver information.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies a device information element that represents the device for which to retrieve driver information. This parameter is optional and can be  <b>NULL</b>. If this parameter is specified, <b>SetupDiGetDriverInfoDetail</b> retrieves information about a driver in a driver list for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiGetDriverInfoDetail</b> retrieves information about a driver that is a member of the global class driver list for <i>DeviceInfoSet</i>.


### -param DriverInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff553287">SP_DRVINFO_DATA</a> structure that specifies the driver information element that represents the driver for which to retrieve details. If <i>DeviceInfoData</i> is specified, the driver must be a member of the driver list for the device that is specified by <i>DeviceInfoData</i>. Otherwise, the driver must be a member of the global class driver list for <i>DeviceInfoSet</i>.


### -param DriverInfoDetailData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff553289">SP_DRVINFO_DETAIL_DATA</a> structure that receives detailed information about the specified driver. If this parameter is not specified, <i>DriverInfoDetailDataSize</i> must be zero. If this parameter is specified, <i>DriverInfoDetailData.</i><b>cbSize</b> must be set to the value of <b>sizeof(</b>SP_DRVINFO_DETAIL_DATA<b>)</b> before it calls <b>SetupDiGetDriverInfoDetail</b>.

<div class="alert"><b>Note</b>  <i>DriverInfoDetailData.</i><b>cbSize</b> must not be set to the value of the <i>DriverInfoDetailDataSize </i>parameter<i>.</i></div>
<div> </div>

### -param DriverInfoDetailDataSize [in]

The size, in bytes, of the <i>DriverInfoDetailData</i> buffer.


### -param RequiredSize [out, optional]

A pointer to a variable that receives the number of bytes required to store the detailed driver information. This value includes both the size of the structure and the additional bytes required for the variable-length character buffer at the end that holds the hardware ID list and the compatible ID list. The lists are in REG_MULTI_SZ format. For information about hardware and compatible IDs, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If the specified driver information member and the caller-supplied buffer are both valid, this function is guaranteed to fill in all static fields in the SP_DRVINFO_DETAIL_DATA structure and as many IDs as possible in the variable-length buffer at the end while still maintaining REG_MULTI_SZ format. In this case, the function returns <b>FALSE</b> and a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER. If specified, <i>RequiredSize</i> contains the total number of bytes required for the structure with all IDs.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551018">SetupDiEnumDriverInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552013">SetupDiGetSelectedDriver</a>
 

 

