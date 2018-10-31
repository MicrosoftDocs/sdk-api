---
UID: NF:setupapi.SetupDiCallClassInstaller
title: SetupDiCallClassInstaller function
author: windows-sdk-content
description: The SetupDiCallClassInstaller function calls the appropriate class installer, and any registered co-installers, with the specified installation request (DIF code).
old-location: devinst\setupdicallclassinstaller.htm
tech.root: devinst
ms.assetid: 2aa631c3-8d00-4309-a37c-efaa7eda3efa
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: SetupDiCallClassInstaller, SetupDiCallClassInstaller function [Device and Driver Installation], devinst.setupdicallclassinstaller, di-rtns_eff914b0-a2db-4eb5-a9b8-f2990efcf252.xml, setupapi/SetupDiCallClassInstaller
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
req.dll: Setupapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-l1-1-0.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-l1-1-1.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDiCallClassInstaller
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiCallClassInstaller function


## -description


The <b>SetupDiCallClassInstaller</b> function calls the appropriate class installer, and any registered co-installers, with the specified installation request (DIF code).


## -parameters




### -param InstallFunction [in]

The device installation request (DIF request) to pass to the co-installers and class installer. DIF codes have the format <b>DIF_<i>XXX</i></b> and are defined in Setupapi.h. See <a href="https://msdn.microsoft.com/f4aadd46-9651-45c3-bec5-65126a7fc9e7">Device Installation Function Codes</a> for more information.

<div class="alert"><b>Note</b>  For certain DIF requests, the caller must be a member of the Administrators group. For such DIF requests, this requirement is listed on the reference page for the associated default handler.</div>
<div> </div>

### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> for the local computer. This set contains a device installation element which represents the device for which to perform the specified installation function. 


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that specifies the device information element in the <i>DeviceInfoSet</i> that represents the device for which to perform the specified installation function. This parameter is optional and can be set to <b>NULL</b>. If this parameter is specified, <b>SetupDiCallClassInstaller</b> performs the specified function on the <i>DeviceInfoData</i> element. If <i>DeviceInfoData</i> is <b>NULL</b>, <b>SetupDiCallClassInstaller</b> calls the installers for the setup class that is associated with <i>DeviceInfoSet</i>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



<b>SetupDiCallClassInstaller</b> calls the class installer and any co-installers that are registered for a device or a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a>. This function loads the installers if they are not yet loaded. The function also calls the default handler for the DIF request, if there is a default handler and if the installers return a status indicating that the default handler should be called.

<a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">Device installation applications</a> call this function with a variety of <a href="https://msdn.microsoft.com/f4aadd46-9651-45c3-bec5-65126a7fc9e7">device installation function codes</a> (DIF codes). The function ensures that all the appropriate installers and default handlers are called, in the correct order, for a given DIF request. For more information, see <a href="devinst.handling_dif_codes">Handling DIF Codes</a>.

After <b>SetupDiCallClassInstaller</b> returns <b>TRUE</b>, the device installation application must call <a href="https://msdn.microsoft.com/e5e8c203-cf71-4cb4-a7a8-5af3a2483eea">SetupDiGetDeviceInstallParams</a> to obtain an <a href="https://msdn.microsoft.com/1bd21150-f8f4-480d-a4b2-99fa4b4233b9">SP_DEVINSTALL_PARAMS</a> structure. If the structure's <b>DI_NEEDREBOOT</b> or <b>DI_NEEDRESTART</b> flag is set, the caller must prompt the user to restart the system. For example, the caller can do this by calling <a href="https://msdn.microsoft.com/14b34fd9-ae96-4552-b99d-488bae5c7644">SetupPromptReboot</a>. 

However, be aware that a device installation application should request a system restart one time at most. Therefore, any device installation application that creates multiple calls to <b>SetupDiCallClassInstaller</b> and <a href="https://msdn.microsoft.com/e5e8c203-cf71-4cb4-a7a8-5af3a2483eea">SetupDiGetDeviceInstallParams</a> should save the <b>DI_NEEDREBOOT</b> and <b>DI_NEEDRESTART</b> flags after each call. However, it should prompt the user only after the last call returns. 

In response to a DIF code supplied by <b>SetupDiCallClassInstaller</b>, class installers and co-installers might perform operations that require the system to be restarted. In such situations, the installer or co-installer should do the following: 

<ol>
<li>
Call <a href="https://msdn.microsoft.com/e5e8c203-cf71-4cb4-a7a8-5af3a2483eea">SetupDiGetDeviceInstallParams</a> to obtain the <a href="https://msdn.microsoft.com/1bd21150-f8f4-480d-a4b2-99fa4b4233b9">SP_DEVINSTALL_PARAMS</a> structure. 

</li>
<li>
Set the <b>DI_NEEDREBOOT</b> or <b>DI_NEEDRESTART</b> flag in the structure's <i>Flags</i> member.

</li>
<li>
Call <a href="https://msdn.microsoft.com/20384538-e124-41f7-94a6-c0fb9f5fe6a0">SetupDiSetDeviceInstallParams</a>, supplying the updated <a href="https://msdn.microsoft.com/1bd21150-f8f4-480d-a4b2-99fa4b4233b9">SP_DEVINSTALL_PARAMS</a> structure, to save the revised <i>Flags</i> member.

</li>
</ol>
After <b>SetupDiCallClassInstaller</b> returns, the device installation application that called it should call <a href="https://msdn.microsoft.com/e5e8c203-cf71-4cb4-a7a8-5af3a2483eea">SetupDiGetDeviceInstallParams</a>, check the flags, and request a restart if necessary.

The device information set specified by <i>DeviceInfoSet</i> must only contain elements for devices on the local computer.

For information about the design and operation of co-installers, see <a href="devinst.writing_a_co_installer">Writing a Co-installer</a>. 




## -see-also




<a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a>
 

 

