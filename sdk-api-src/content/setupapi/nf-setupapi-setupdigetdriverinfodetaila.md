---
UID: NF:setupapi.SetupDiGetDriverInfoDetailA
title: SetupDiGetDriverInfoDetailA function
author: windows-sdk-content
description: The SetupDiGetDriverInfoDetail function retrieves driver information detail for a device information set or a particular device information element in the device information set.
old-location: devinst\setupdigetdriverinfodetail.htm
tech.root: devinst
ms.assetid: 42f3668c-8112-4cc0-bce8-b0b3886c45fb
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: SetupDiGetDriverInfoDetail, SetupDiGetDriverInfoDetail function [Device and Driver Installation], SetupDiGetDriverInfoDetailA, SetupDiGetDriverInfoDetailW, devinst.setupdigetdriverinfodetail, di-rtns_5a2fb98d-54ee-4290-9969-f5e12d77cbcf.xml, setupapi/SetupDiGetDriverInfoDetail
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Setupapi.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# SetupDiGetDriverInfoDetailA function


## -description


The <b>SetupDiGetDriverInfoDetail</b> function retrieves driver information detail for a device information set or a particular device information element in the device information set.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="https://msdn.microsoft.com/library/Ff541247(v=VS.85).aspx">device information set</a> that contains a driver information element for which to retrieve driver information.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that specifies a device information element that represents the device for which to retrieve driver information. This parameter is optional and can be  <b>NULL</b>. If this parameter is specified, <b>SetupDiGetDriverInfoDetail</b> retrieves information about a driver in a driver list for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiGetDriverInfoDetail</b> retrieves information about a driver that is a member of the global class driver list for <i>DeviceInfoSet</i>.


### -param DriverInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/13cdebad-6247-4651-a1d0-709e14af22f6">SP_DRVINFO_DATA</a> structure that specifies the driver information element that represents the driver for which to retrieve details. If <i>DeviceInfoData</i> is specified, the driver must be a member of the driver list for the device that is specified by <i>DeviceInfoData</i>. Otherwise, the driver must be a member of the global class driver list for <i>DeviceInfoSet</i>.


### -param DriverInfoDetailData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/6e16a90a-a876-471c-917b-a26229a9187a">SP_DRVINFO_DETAIL_DATA</a> structure that receives detailed information about the specified driver. If this parameter is not specified, <i>DriverInfoDetailDataSize</i> must be zero. If this parameter is specified, <i>DriverInfoDetailData.</i><b>cbSize</b> must be set to the value of <b>sizeof(</b>SP_DRVINFO_DETAIL_DATA<b>)</b> before it calls <b>SetupDiGetDriverInfoDetail</b>.

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




<a href="https://msdn.microsoft.com/c4a66d0c-e9a9-41f8-87df-576795667b5c">SetupDiEnumDriverInfo</a>



<a href="https://msdn.microsoft.com/dd3d9736-755c-497c-a523-18ca66557ae7">SetupDiGetSelectedDriver</a>
 

 

