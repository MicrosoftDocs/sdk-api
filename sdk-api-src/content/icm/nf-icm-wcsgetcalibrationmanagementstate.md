---
UID: NF:icm.WcsGetCalibrationManagementState
title: WcsGetCalibrationManagementState function
author: windows-driver-content
description: Determines whether system management of the display calibration state is enabled.
old-location: wcs\wcsgetcalibrationmanagementstate.htm
old-project: WCS
ms.assetid: 1c069d20-3d99-497f-bd43-613b504355d8
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: WcsGetCalibrationManagementState, WcsGetCalibrationManagementState function [Windows Color System], icm/WcsGetCalibrationManagementState, wcs.wcsgetcalibrationmanagementstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
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
req.typenames: WCS_PROFILE_MANAGEMENT_SCOPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mscms.dll
api_name:
-	WcsGetCalibrationManagementState
product: Windows
targetos: Windows
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
req.product: GDI+ 1.1
---

# WcsGetCalibrationManagementState function


## -description


Determines whether system management of the display calibration state is enabled.


## -parameters




### -param pbIsEnabled [out]

<b>TRUE</b> if system management of the display calibration state is enabled; otherwise <b>FALSE</b>.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>.



