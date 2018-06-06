---
UID: NF:cfgmgr32.CM_MapCrToWin32Err
title: CM_MapCrToWin32Err function
author: windows-sdk-content
description: Converts a specified CONFIGRET code to its equivalent system error code.
old-location: devinst\cm_mapcrtowin32err.htm
old-project: devinst
ms.assetid: 7FC862D9-124D-413A-9082-F524E172FBDC
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: CM_MapCrToWin32Err, CM_MapCrToWin32Err function [Device and Driver Installation], cfgmgr32/CM_MapCrToWin32Err, devinst.cm_mapcrtowin32err
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfgmgr32.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 7 and later versions of Windows.
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
 - API-MS-Win-devices-config-L1-1-1.dll
api_name:
 - CM_MapCrToWin32Err
product: Windows
targetos: Windows
req.lib: CfgMgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
---

# CM_MapCrToWin32Err function


## -description


Converts a specified <b>CONFIGRET</b> code to its equivalent system error 
    code.


## -parameters




### -param CmReturnCode [in]

The <b>CONFIGRET</b> code to be converted. <b>CONFIGRET</b> 
      error codes are defined in CfgMgr32.h.


### -param DefaultErr [in]

A default system error code to be returned when no system error code is mapped to the specified 
      <b>CONFIGRET</b> code.


## -returns



The system error code that corresponds to the <b>CONFIGRET</b> code. System error codes 
       are defined in Winerror.h.

When there is no mapping from the specified <b>CONFIGRET</b> code to a system error 
       code, <b>CM_MapCrToWin32Err</b> returns the value 
       specified in the <i>DefaultErr</i> parameter.



