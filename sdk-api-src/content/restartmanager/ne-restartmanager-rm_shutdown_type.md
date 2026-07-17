---
UID: NE:restartmanager._RM_SHUTDOWN_TYPE
title: RM_SHUTDOWN_TYPE (restartmanager.h)
description: Configures the shut down of applications.
helpviewer_keywords: ["RM_SHUTDOWN_TYPE","RmForceShutdown","RmShutdownOnlyRegistered","_RM_SHUTDOWN_TYPE","_RM_SHUTDOWN_TYPE enumeration [Restart Mgr]","restartmanager/RmForceShutdown","restartmanager/RmShutdownOnlyRegistered","restartmanager/_RM_SHUTDOWN_TYPE","rstmgr.rm_shutdown_type"]
old-location: rstmgr\rm_shutdown_type.htm
tech.root: rstmgr
ms.assetid: e75f60a3-535b-4c1f-85ae-37f4c4c71ede
ms.date: 12/05/2018
ms.keywords: RM_SHUTDOWN_TYPE, RmForceShutdown, RmShutdownOnlyRegistered, _RM_SHUTDOWN_TYPE, _RM_SHUTDOWN_TYPE enumeration [Restart Mgr], restartmanager/RmForceShutdown, restartmanager/RmShutdownOnlyRegistered, restartmanager/_RM_SHUTDOWN_TYPE, rstmgr.rm_shutdown_type
req.header: restartmanager.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RM_SHUTDOWN_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RM_SHUTDOWN_TYPE
 - restartmanager/_RM_SHUTDOWN_TYPE
 - RM_SHUTDOWN_TYPE
 - restartmanager/RM_SHUTDOWN_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RestartManager.h
api_name:
 - RM_SHUTDOWN_TYPE
---

# RM_SHUTDOWN_TYPE enumeration


## -description

 Configures the shut down of applications.

## -enum-fields

### -field RmForceShutdown:0x1

 Forces unresponsive applications and services to shut down after the timeout period. An application that does not respond to a shutdown request by the Restart Manager is forced to shut down after 30 seconds. A service that does not respond to a shutdown request is forced to shut down after 20 seconds. These default times can be changed by modifying the registry keys described in the Remarks section.

### -field RmShutdownOnlyRegistered:0x10 

Shuts down applications if and only if all the applications have been registered for restart  using the <b>RegisterApplicationRestart</b> function. If any processes or services cannot be restarted, then no processes or services are shut down.

## -remarks

The time to wait before initiating a forced shutdown of applications can be obtained by calling the
<a href="/windows/win32/api/winuser/nf-winuser-systemparametersinfow">SystemParametersInfo</a> function
with the value <b>SPI_GETHUNGAPPTIMEOUT</b>.

The time to wait before initiating a forced shutdown of services can be obtained by calling the
<a href="/windows/win32/api/winuser/nf-winuser-systemparametersinfow">SystemParametersInfo</a> function
with the value <b>SPI_GETWAITTOKILLSERVICETIMEOUT</b>.

## -see-also

<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmshutdown">RmShutdown</a>
