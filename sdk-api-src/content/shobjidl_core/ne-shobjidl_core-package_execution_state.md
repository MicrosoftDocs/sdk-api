---
UID: NE:shobjidl_core.PACKAGE_EXECUTION_STATE
title: PACKAGE_EXECUTION_STATE (shobjidl_core.h)
description: .helpviewer_keywords: ["PACKAGE_EXECUTION_STATE","PACKAGE_EXECUTION_STATE enumeration [Windows Shell]","PES_RUNNING","PES_SUSPENDED","PES_SUSPENDING","PES_TERMINATED","PES_UNKNOWN","shell.PACKAGE_EXECUTION_STATE","shobjidl_core/PACKAGE_EXECUTION_STATE","shobjidl_core/PES_RUNNING","shobjidl_core/PES_SUSPENDED","shobjidl_core/PES_SUSPENDING","shobjidl_core/PES_TERMINATED","shobjidl_core/PES_UNKNOWN"]
old-location: shell\PACKAGE_EXECUTION_STATE.htm
tech.root: shell
ms.assetid: 8BE433AC-34E6-42D7-9F8B-63AECAC96996
ms.date: 12/05/2018
ms.keywords: PACKAGE_EXECUTION_STATE, PACKAGE_EXECUTION_STATE enumeration [Windows Shell], PES_RUNNING, PES_SUSPENDED, PES_SUSPENDING, PES_TERMINATED, PES_UNKNOWN, shell.PACKAGE_EXECUTION_STATE, shobjidl_core/PACKAGE_EXECUTION_STATE, shobjidl_core/PES_RUNNING, shobjidl_core/PES_SUSPENDED, shobjidl_core/PES_SUSPENDING, shobjidl_core/PES_TERMINATED, shobjidl_core/PES_UNKNOWN
f1_keywords:
- shobjidl_core/PACKAGE_EXECUTION_STATE
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
- HeaderDef
api_location:
- shobjidl_core.h
api_name:
- PACKAGE_EXECUTION_STATE
targetos: Windows
req.typenames: PACKAGE_EXECUTION_STATE
req.redist: 
ms.custom: 19H1
---

# PACKAGE_EXECUTION_STATE enumeration


## -description

Represents the state of a Windows app package.



## -enum-fields




### -field PES_UNKNOWN

The package is in an unknown state.

### -field PES_RUNNING

The package is running.


### -field PES_SUSPENDING

The package is being suspended.

### -field PES_SUSPENDED

The package is suspended.

### -field PES_TERMINATED

The package was terminated.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-getpackageexecutionstate">IPackageIPackageDebugSettings::GetPackageExecutionState</a>

<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackageexecutionstatechangenotification-onstatechanged">IPackageExecutionStateChangeNotification::OnStateChanged</a>
