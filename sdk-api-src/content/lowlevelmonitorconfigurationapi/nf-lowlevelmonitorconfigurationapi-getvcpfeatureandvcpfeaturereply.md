---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# GetVCPFeatureAndVCPFeatureReply function


## -description



        Retrieves the current value, maximum value, and code type of a Virtual Control Panel (VCP) code for a monitor.


## -parameters




### -param hMonitor [in]


            Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param bVCPCode [in]


            VCP code to query. The VCP codes are Include the VESA Monitor Control Command Set (MCCS) standard, versions 1.0 and 2.0. This parameter must specify a continuous or non-continuous VCP, or a vendor-specific code. It should not be a table control code.
          


### -param pvct [out]


            Receives the VCP code type, as a member of the <a href="https://msdn.microsoft.com/2ccfd6d0-7885-45b7-b44f-edefa320b881">MC_VCP_CODE_TYPE</a> enumeration. This parameter can be <b>NULL</b>.
          


### -param pdwCurrentValue [out]


            Receives the current value of the VCP code. This parameter can be <b>NULL</b>.
          


### -param pdwMaximumValue [out]


            If <i>bVCPCode</i> specifies a continuous VCP code, this parameter receives the maximum value of the VCP code. If <i>bVCPCode</i> specifies a non-continuous VCP code, the value received in this parameter is undefined. This parameter can be <b>NULL</b>.
          


## -returns




            If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks




        This function corresponds to the "Get VCP Feature &amp; VCP Feature Reply" command from the Display Data Channel Command Interface (DDC/CI) standard. Vendor-specific VCP codes can be used with this function.
      


        This function takes about 40 milliseconds to return.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

