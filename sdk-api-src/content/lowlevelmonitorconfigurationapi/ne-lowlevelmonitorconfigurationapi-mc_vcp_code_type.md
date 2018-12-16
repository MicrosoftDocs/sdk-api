---
UID: NE:lowlevelmonitorconfigurationapi._MC_VCP_CODE_TYPE
title: MC_VCP_CODE_TYPE
author: windows-sdk-content
description: Describes a Virtual Control Panel (VCP) code type.
old-location: monitor\mc_vcp_code_type.htm
tech.root: Monitor
ms.assetid: 2ccfd6d0-7885-45b7-b44f-edefa320b881
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPMC_VCP_CODE_TYPE, LPMC_VCP_CODE_TYPE, LPMC_VCP_CODE_TYPE enumeration pointer [Monitor Configuration], MC_MOMENTARY, MC_SET_PARAMETER, MC_VCP_CODE_TYPE, MC_VCP_CODE_TYPE , MC_VCP_CODE_TYPE enumeration [Monitor Configuration], lowlevelmonitorconfigurationapi/LPMC_VCP_CODE_TYPE, lowlevelmonitorconfigurationapi/MC_MOMENTARY, lowlevelmonitorconfigurationapi/MC_SET_PARAMETER, lowlevelmonitorconfigurationapi/MC_VCP_CODE_TYPE, monitor.mc_vcp_code_type"
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LowLevelMonitorConfigurationAPI.h
api_name:
 - MC_VCP_CODE_TYPE
product: Windows
targetos: Windows
req.typenames: MC_VCP_CODE_TYPE, *LPMC_VCP_CODE_TYPE
req.redist: 
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




<a href="https://msdn.microsoft.com/b0b06137-8f67-46fc-ba6b-3022f3331fa5">GetVCPFeatureAndVCPFeatureReply</a>



<a href="https://msdn.microsoft.com/d6ab74af-0ac4-4dfe-bbf8-21b8339d2826">Monitor Configuration Enumeration Types</a>



<a href="https://msdn.microsoft.com/0c3acb13-c5db-44ce-937d-b0b001a08062">SetMonitorDisplayAreaSize</a>
 

 

