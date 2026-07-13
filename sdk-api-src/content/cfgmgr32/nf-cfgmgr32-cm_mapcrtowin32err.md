---
UID: NF:cfgmgr32.CM_MapCrToWin32Err
title: CM_MapCrToWin32Err function (cfgmgr32.h)
description: Converts a specified CONFIGRET code to its equivalent system error code.
helpviewer_keywords: ["CM_MapCrToWin32Err","CM_MapCrToWin32Err function [Device and Driver Installation]","cfgmgr32/CM_MapCrToWin32Err","devinst.cm_mapcrtowin32err"]
old-location: devinst\cm_mapcrtowin32err.htm
tech.root: devinst
ms.assetid: 7FC862D9-124D-413A-9082-F524E172FBDC
ms.date: 12/05/2018
ms.keywords: CM_MapCrToWin32Err, CM_MapCrToWin32Err function [Device and Driver Installation], cfgmgr32/CM_MapCrToWin32Err, devinst.cm_mapcrtowin32err
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
req.lib: CfgMgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_MapCrToWin32Err
 - cfgmgr32/CM_MapCrToWin32Err
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
 - API-MS-Win-devices-config-L1-1-1.dll
api_name:
 - CM_MapCrToWin32Err
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

