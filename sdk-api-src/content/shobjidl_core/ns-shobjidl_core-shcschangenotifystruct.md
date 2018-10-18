---
UID: NS:shobjidl_core.SHCSCHANGENOTIFYSTRUCT
title: SHCSCHANGENOTIFYSTRUCT
author: windows-sdk-content
description: Contains information about change notification. It is used by IShellMenuCallback::CallbackSM.
old-location: shell\SMCSHCHANGENOTIFYSTRUCT.htm
tech.root: shell
ms.assetid: 31fd2550-d39c-45fc-9c19-6ba2858002de
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: "*PSMCSHCHANGENOTIFYSTRUCT, PSMCSHCHANGENOTIFYSTRUCT, PSMCSHCHANGENOTIFYSTRUCT structure pointer [Windows Shell], SHCSCHANGENOTIFYSTRUCT, SMCSHCHANGENOTIFYSTRUCT, SMCSHCHANGENOTIFYSTRUCT structure [Windows Shell], _win32_SMCSHCHANGENOTIFYSTRUCT, shell.SMCSHCHANGENOTIFYSTRUCT, shobjidl_core/PSMCSHCHANGENOTIFYSTRUCT, shobjidl_core/SMCSHCHANGENOTIFYSTRUCT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SMCSHCHANGENOTIFYSTRUCT
product: Windows
targetos: Windows
req.typenames: SMCSHCHANGENOTIFYSTRUCT, *PSMCSHCHANGENOTIFYSTRUCT
req.redist: 
---

# SHCSCHANGENOTIFYSTRUCT structure


## -description


Contains information about change notification. It is used by <a href="https://msdn.microsoft.com/06809b61-041b-41bd-82dd-0d64edf8bbae">IShellMenuCallback::CallbackSM</a>.


## -struct-fields




### -field lEvent

Type: <b>long</b>

An SHCNE value that specifies the type of change that took place. See <a href="https://msdn.microsoft.com/a9222ce9-0d06-4fd0-af3a-fd0e979713ce">SHChangeNotify</a> for a complete list of these values.


### -field pidl1

Type: <b>PCIDLIST_ABSOLUTE</b>

PIDL provided by the change notification. The target of this PIDL varies depending on the value of <b>lEvent</b>.


### -field pidl2

Type: <b>PCIDLIST_ABSOLUTE</b>

A second PIDL provided by the change notification. Not all <b>lEvent</b> values make use of this parameter, in which case its value is <b>NULL</b>.

