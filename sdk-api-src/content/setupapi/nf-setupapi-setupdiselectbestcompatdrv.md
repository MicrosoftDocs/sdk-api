---
UID: NF:setupapi.SetupDiSelectBestCompatDrv
title: SetupDiSelectBestCompatDrv function (setupapi.h)
description: The SetupDiSelectBestCompatDrv function is the default handler for the DIF_SELECTBESTCOMPATDRV installation request.
helpviewer_keywords: ["SetupDiSelectBestCompatDrv","SetupDiSelectBestCompatDrv function [Device and Driver Installation]","devinst.setupdiselectbestcompatdrv","di-rtns_3dee9465-1e0f-4efc-beb2-280c6b2621e9.xml","setupapi/SetupDiSelectBestCompatDrv"]
old-location: devinst\setupdiselectbestcompatdrv.htm
tech.root: devinst
ms.assetid: fef435a6-b6cd-47be-bf63-358478ec3cb6
ms.date: 12/05/2018
ms.keywords: SetupDiSelectBestCompatDrv, SetupDiSelectBestCompatDrv function [Device and Driver Installation], devinst.setupdiselectbestcompatdrv, di-rtns_3dee9465-1e0f-4efc-beb2-280c6b2621e9.xml, setupapi/SetupDiSelectBestCompatDrv
f1_keywords:
- setupapi/SetupDiSelectBestCompatDrv
dev_langs:
- c++
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows 2000 and later versions of Windows.
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
req.dll: Setupapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Setupapi.dll
api_name:
- SetupDiSelectBestCompatDrv
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupDiSelectBestCompatDrv function


## -description


The <b>SetupDiSelectBestCompatDrv</b> function is the default handler for the <a href="https://docs.microsoft.com/windows-hardware/drivers/install/dif-selectbestcompatdrv">DIF_SELECTBESTCOMPATDRV</a> installation request.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="https://docs.microsoft.com/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a device information element that represents the device for which to select the best compatible driver.


### -param DeviceInfoData [in, out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. <b>SetupDiSelectBestCompatDrv</b> selects the best driver for a device information element from the compatible driver list for the specified device. 


## -returns



If the operation succeeds, <b>SetupDiSelectBestCompatDrv</b> returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="https://msdn.microsoft.com/library/ms679360(VS.85).aspx">GetLastError</a>.




## -remarks



If the caller of <b>SetupDiSelectBestCompatDrv</b> is a member of the Administrators group and the class of the device is different that the class of the selected driver, <b>SetupDiSelectBestCompatDrv</b> sets the class of the device to the class of the driver. If this behavior is not desired, call this function at a lower privilege level. 

<div class="alert"><b>Note</b>  Only a class installer should call <b>SetupDiSelectBestCompatDrv</b> and only in those situations where the class installer must perform driver selection operations after <b>SetupDiSelectBestCompatDrv</b> completes the default driver selection operation. In such situations, the class installer must directly call <b>SetupDiSelectBestCompatDrv</b> when the installer processes a DIF_SELECTBESTCOMPATDRV request. For more information about calling the default handler, see <a href="https://docs.microsoft.com/windows-hardware/drivers/install/calling-the-default-dif-code-handlers">Calling Default DIF Code Handlers</a>.</div>
<div> </div>
<b>SetupDiSelectBestCompatDrv </b>is primarily designed to select the best compatible driver for a device information element on a local computer. Although <b>SetupDiSelectBestCompatDrv </b>will not fail if the device information set is for a remote computer, the result is of limited use because the device information set cannot subsequently be used as input with DIF_<i>Xxx</i> installation requests or <b>SetupDi</b><i>Xxx</i> functions that do not support operations for a remote computer. In particular, the device information set cannot subsequently be used as input with a DIF_INSTALLDEVICE installation request to install a device on a remote computer.

For information about how the best driver is selected, see <a href="https://docs.microsoft.com/windows-hardware/drivers/install/how-setup-selects-drivers">How Windows Selects Drivers</a>.

To get the selected driver for a device, call <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdigetselecteddrivera">SetupDiGetSelectedDriver</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/install/dif-selectbestcompatdrv">DIF_SELECTBESTCOMPATDRV</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a>
 

 

