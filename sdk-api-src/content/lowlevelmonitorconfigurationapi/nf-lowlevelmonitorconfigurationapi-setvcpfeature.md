---
UID: NF:lowlevelmonitorconfigurationapi.SetVCPFeature
title: SetVCPFeature function
author: windows-sdk-content
description: Sets the value of a Virtual Control Panel (VCP) code for a monitor.
old-location: monitor\setvcpfeature.htm
old-project: Monitor
ms.assetid: 145c393e-dce0-4d50-94c2-61ba580c3d83
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: SetVCPFeature, SetVCPFeature function [Monitor Configuration], lowlevelmonitorconfigurationapi/SetVCPFeature, monitor.setvcpfeature
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: MC_VCP_CODE_TYPE, *LPMC_VCP_CODE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - SetVCPFeature
product: Windows
targetos: Windows
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetVCPFeature function


## -description



        Sets the value of a Virtual Control Panel (VCP) code for a monitor.


## -parameters




### -param hMonitor [in]


            Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param bVCPCode [in]


            VCP code to set. The VCP codes are defined in the VESA Monitor Control Command Set (MCCS) standard, version 1.0 and 2.0. This parameter must specify a continuous or non-continuous VCP, or a vendor-specific code. It should not be a table control code.
          


### -param dwNewValue [in]


            Value of the VCP code.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call GetLastError.




## -remarks




        This function corresponds to the "Set VCP Feature" command from the Display Data Channel Command Interface (DDC/CI) standard.
      


        This function takes about 50 milliseconds to return.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

