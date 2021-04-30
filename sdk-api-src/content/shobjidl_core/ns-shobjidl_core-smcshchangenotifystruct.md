---
UID: NS:shobjidl_core.SHCSCHANGENOTIFYSTRUCT
title: SMCSHCHANGENOTIFYSTRUCT (shobjidl_core.h)
description: Contains information about change notification. It is used by IShellMenuCallback::CallbackSM.
helpviewer_keywords: ["*PSMCSHCHANGENOTIFYSTRUCT","PSMCSHCHANGENOTIFYSTRUCT","PSMCSHCHANGENOTIFYSTRUCT structure pointer [Windows Shell]","SHCSCHANGENOTIFYSTRUCT","SMCSHCHANGENOTIFYSTRUCT","SMCSHCHANGENOTIFYSTRUCT structure [Windows Shell]","_win32_SMCSHCHANGENOTIFYSTRUCT","shell.SMCSHCHANGENOTIFYSTRUCT","shobjidl_core/PSMCSHCHANGENOTIFYSTRUCT","shobjidl_core/SMCSHCHANGENOTIFYSTRUCT"]
old-location: shell\SMCSHCHANGENOTIFYSTRUCT.htm
tech.root: shell
ms.assetid: 31fd2550-d39c-45fc-9c19-6ba2858002de
ms.date: 12/05/2018
ms.keywords: '*PSMCSHCHANGENOTIFYSTRUCT, PSMCSHCHANGENOTIFYSTRUCT, PSMCSHCHANGENOTIFYSTRUCT structure pointer [Windows Shell], SHCSCHANGENOTIFYSTRUCT, SMCSHCHANGENOTIFYSTRUCT, SMCSHCHANGENOTIFYSTRUCT structure [Windows Shell], _win32_SMCSHCHANGENOTIFYSTRUCT, shell.SMCSHCHANGENOTIFYSTRUCT, shobjidl_core/PSMCSHCHANGENOTIFYSTRUCT, shobjidl_core/SMCSHCHANGENOTIFYSTRUCT'
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.h
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SMCSHCHANGENOTIFYSTRUCT, *PSMCSHCHANGENOTIFYSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCSCHANGENOTIFYSTRUCT
 - shobjidl_core/SHCSCHANGENOTIFYSTRUCT
 - PSMCSHCHANGENOTIFYSTRUCT
 - shobjidl_core/PSMCSHCHANGENOTIFYSTRUCT
 - SMCSHCHANGENOTIFYSTRUCT
 - shobjidl_core/SMCSHCHANGENOTIFYSTRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SMCSHCHANGENOTIFYSTRUCT
---

# SMCSHCHANGENOTIFYSTRUCT structure


## -description

Contains information about change notification. It is used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm">IShellMenuCallback::CallbackSM</a>.

## -struct-fields

### -field lEvent

Type: <b>long</b>

An SHCNE value that specifies the type of change that took place. See <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify">SHChangeNotify</a> for a complete list of these values.

### -field pidl1

Type: <b>PCIDLIST_ABSOLUTE</b>

PIDL provided by the change notification. The target of this PIDL varies depending on the value of <b>lEvent</b>.

### -field pidl2

Type: <b>PCIDLIST_ABSOLUTE</b>

A second PIDL provided by the change notification. Not all <b>lEvent</b> values make use of this parameter, in which case its value is <b>NULL</b>.