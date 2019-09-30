---
UID: NF:setupapi.SetupDiChangeState
title: SetupDiChangeState function (setupapi.h)
author: windows-sdk-content
description: The SetupDiChangeState function is the default handler for the DIF_PROPERTYCHANGE installation request.
old-location: devinst\setupdichangestate.htm
tech.root: devinst
ms.assetid: 204c1366-1817-4cd1-a1fd-a4ad3e79b7cc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupDiChangeState, SetupDiChangeState function [Device and Driver Installation], devinst.setupdichangestate, di-rtns_0749286d-9e78-4e2a-8bbf-483d698753ba.xml, setupapi/SetupDiChangeState
ms.topic: function
f1_keywords:
- setupapi/SetupDiChangeState
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
req.dll: Setupapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Setupapi.dll
- Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
- SetupDiChangeState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupDiChangeState function


## -description


The <b>SetupDiChangeState</b> function is the default handler for the <a href="https://docs.microsoft.com/windows-hardware/drivers/install/dif-propertychange">DIF_PROPERTYCHANGE</a> installation request. 


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="https://docs.microsoft.com/windows-hardware/drivers/install/device-information-sets">device information set</a> for the local computer. This set contains a device information element that represents the device whose state is to be changed. 


### -param DeviceInfoData [in, out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. This is an IN-OUT parameter because <i>DeviceInfoData.</i><b>DevInst</b> might be updated with a new handle value upon return.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



<b>SetupDiChangeState</b> changes the state of an installed device.

The caller of <b>SetupDiChangeState</b> must be a member of the Administrators group.

<div class="alert"><b>Note</b>  Only a class installer should call <b>SetupDiChangeState</b> and only in those situations where the class installer must perform property change operations after <b>SetupDiChangeState</b> completes the default property change operation. In such situations, the class installer must directly call <b>SetupDiChangeState</b> when the installer processes a DIF_PROPERTYCHANGE request. For more information about calling the default handler, see <a href="https://docs.microsoft.com/windows-hardware/drivers/install/calling-the-default-dif-code-handlers">Calling Default DIF Code Handlers</a>.</div>
<div> </div>
Callers of <b>SetupDiChangeState</b> must specify a DICS_<i>XXX</i> flag in the <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_propchange_params">SP_PROPCHANGE_PARAMS</a> for the device element that indicates the type of state change to perform on the device. Callers of this function must set the appropriate fields in the SP_PROPCHANGE_PARAMS and call <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdisetclassinstallparamsa">SetupDiSetClassInstallParams</a> before calling this function.

If you specify the DICS_FLAG_CONFIGSPECIFIC flag in the SP_PROPCHANGE_PARAMS then you must fill in the <b>HwProfile</b> field. A value of zero for <b>HwProfile</b> indicates the current profile. 

To enable/disable a device in the current hardware profile, set the DICS_FLAG_CONFIGSPECIFIC flag in the SP_PROPCHANGE_PARAMS. To enable/disable a device globally, such as in both the docked and undocked hardware profiles, set the DICS_FLAG_GLOBAL flag.

This function does the following:



Callers of this function should not specify DICS_STOP or DICS_START in the SP_PROPCHANGE_PARAMS. Use DICS_PROPCHANGE to stop and restart a device to cause changes in the device's configuration to take effect.

If DI_DONOTCALLCONFIGMG is set for a device, you should not call <b>SetupDiChangeState</b> for the device but should instead set the DI_NEEDREBOOT flag. 




## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/install/dif-propertychange">DIF_PROPERTYCHANGE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_propchange_params">SP_PROPCHANGE_PARAMS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>
 

 

