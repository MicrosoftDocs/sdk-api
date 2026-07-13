---
UID: NF:cfgmgr32.CM_Disable_DevNode
title: CM_Disable_DevNode function (cfgmgr32.h)
description: The CM_Disable_DevNode function disables a device.
helpviewer_keywords: ["CM_Disable_DevNode","CM_Disable_DevNode function [Device and Driver Installation]","cfgmgr32/CM_Disable_DevNode","cfgmgrfn_3a8b48b2-fb94-421c-9ec4-2e88997eb9b5.xml","devinst.cm_disable_devnode"]
old-location: devinst\cm_disable_devnode.htm
tech.root: devinst
ms.assetid: 6013fec3-1fb3-4956-982d-5841518f5d31
ms.date: 07/09/2025
ms.keywords: CM_Disable_DevNode, CM_Disable_DevNode function [Device and Driver Installation], cfgmgr32/CM_Disable_DevNode, cfgmgrfn_3a8b48b2-fb94-421c-9ec4-2e88997eb9b5.xml, devinst.cm_disable_devnode
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.lib: Cfgmgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Disable_DevNode
 - cfgmgr32/CM_Disable_DevNode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-devices-config-l1-1-2.dll
 - CfgMgr32.dll
 - API-MS-Win-devices-config-l1-1-0.dll
 - API-MS-Win-devices-config-l1-1-1.dll
api_name:
 - CM_Disable_DevNode
---

# CM_Disable_DevNode function


## -description

The <b>CM_Disable_DevNode</b> function disables a device.

## -parameters

### -param dnDevInst [in]

Device instance handle that is bound to the local machine.

### -param ulFlags [in]

Disable flags:





#### CM_DISABLE_UI_NOT_OK

Do not display any interface to the user if the attempt to disable the device fails.



#### CM_DISABLE_PERSIST (Windows 10 and later versions of Windows)

Disables the device across reboots.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

By default, <b>CM_Disable_DevNode</b> disables a device at one time, but after reboot the device is enabled again. Starting in Windows 10, you can specify the <b>CM_DISABLE_PERSIST</b> flag to disable the device across reboots.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_enable_devnode">CM_Enable_DevNode</a>



<a href="/windows-hardware/drivers/install/dif-propertychange">DIF_PROPERTYCHANGE</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>