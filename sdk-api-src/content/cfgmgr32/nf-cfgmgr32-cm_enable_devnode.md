---
UID: NF:cfgmgr32.CM_Enable_DevNode
title: CM_Enable_DevNode function
author: windows-sdk-content
description: The CM_Enable_DevNode function enables a device.
old-location: devinst\cm_enable_devnode.htm
old-project: devinst
ms.assetid: ddc3a507-03ee-4f44-89e3-64ec4290d0ff
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: CM_Enable_DevNode, CM_Enable_DevNode function [Device and Driver Installation], cfgmgr32/CM_Enable_DevNode, cfgmgrfn_10a592e0-91c9-47f2-aaa1-769e44bc1cbc.xml, devinst.cm_enable_devnode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: CM_NOTIFY_ACTION, *PCM_NOTIFY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CfgMgr32.dll
 - API-MS-Win-devices-config-l1-1-0.dll
 - API-MS-Win-devices-config-l1-1-1.dll
api_name:
 - CM_Enable_DevNode
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
---

# CM_Enable_DevNode function


## -description


The <b>CM_Enable_DevNode</b> function enables a device.


## -parameters




### -param dnDevInst [in]

Device instance handle that is bound to the local machine.


### -param ulFlags [in]

Reserved. Must be set to zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537996">CM_Disable_DevNode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543712">DIF_PROPERTYCHANGE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a>
 

 

