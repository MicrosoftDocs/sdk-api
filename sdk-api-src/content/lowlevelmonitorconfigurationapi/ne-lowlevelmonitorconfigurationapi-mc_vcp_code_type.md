---
UID: NE:lowlevelmonitorconfigurationapi._MC_VCP_CODE_TYPE
title: MC_VCP_CODE_TYPE (lowlevelmonitorconfigurationapi.h)
description: Describes a Virtual Control Panel (VCP) code type.
helpviewer_keywords: ["*LPMC_VCP_CODE_TYPE","LPMC_VCP_CODE_TYPE","LPMC_VCP_CODE_TYPE enumeration pointer [Monitor Configuration]","MC_MOMENTARY","MC_SET_PARAMETER","MC_VCP_CODE_TYPE","MC_VCP_CODE_TYPE","MC_VCP_CODE_TYPE enumeration [Monitor Configuration]","lowlevelmonitorconfigurationapi/LPMC_VCP_CODE_TYPE","lowlevelmonitorconfigurationapi/MC_MOMENTARY","lowlevelmonitorconfigurationapi/MC_SET_PARAMETER","lowlevelmonitorconfigurationapi/MC_VCP_CODE_TYPE","monitor.mc_vcp_code_type"]
old-location: monitor\mc_vcp_code_type.htm
tech.root: Monitor
ms.assetid: 2ccfd6d0-7885-45b7-b44f-edefa320b881
ms.date: 12/05/2018
ms.keywords: '*LPMC_VCP_CODE_TYPE, LPMC_VCP_CODE_TYPE, LPMC_VCP_CODE_TYPE enumeration pointer [Monitor Configuration], MC_MOMENTARY, MC_SET_PARAMETER, MC_VCP_CODE_TYPE, MC_VCP_CODE_TYPE , MC_VCP_CODE_TYPE enumeration [Monitor Configuration], lowlevelmonitorconfigurationapi/LPMC_VCP_CODE_TYPE, lowlevelmonitorconfigurationapi/MC_MOMENTARY, lowlevelmonitorconfigurationapi/MC_SET_PARAMETER, lowlevelmonitorconfigurationapi/MC_VCP_CODE_TYPE, monitor.mc_vcp_code_type'
req.header: lowlevelmonitorconfigurationapi.h
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
req.typenames: MC_VCP_CODE_TYPE, *LPMC_VCP_CODE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MC_VCP_CODE_TYPE
 - lowlevelmonitorconfigurationapi/_MC_VCP_CODE_TYPE
 - LPMC_VCP_CODE_TYPE
 - lowlevelmonitorconfigurationapi/LPMC_VCP_CODE_TYPE
 - MC_VCP_CODE_TYPE
 - lowlevelmonitorconfigurationapi/MC_VCP_CODE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LowLevelMonitorConfigurationAPI.h
api_name:
 - MC_VCP_CODE_TYPE
---

# MC_VCP_CODE_TYPE enumeration


## -description

Describes a Virtual Control Panel (VCP) code type.

## -enum-fields

### -field MC_MOMENTARY

Momentary VCP code. Sending a command of this type causes the monitor to initiate a self-timed operation and then revert to its original state. Examples include display tests and degaussing.

### -field MC_SET_PARAMETER

Set Parameter VCP code. Sending a command of this type changes some aspect of the monitor's operation.

## -see-also

<a href="/windows/desktop/api/lowlevelmonitorconfigurationapi/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply">GetVCPFeatureAndVCPFeatureReply</a>



<a href="/windows/desktop/Monitor/monitor-configuration-enumeration-types">Monitor Configuration Enumeration Types</a>



<a href="/windows/desktop/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitordisplayareasize">SetMonitorDisplayAreaSize</a>