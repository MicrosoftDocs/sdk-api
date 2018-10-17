---
UID: NF:mfidl.MFCreateSensorProfile
title: MFCreateSensorProfile function
author: windows-sdk-content
description: Creates a sensor profile, based on the specified type, index, and optional constraints.
old-location: mf\mfcreatesensorprofile.htm
tech.root: medfound
ms.assetid: 76D14E98-0DB5-4D2C-9F6A-17D9B3CAA73E
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: MFCreateSensorProfile, MFCreateSensorProfile function [Media Foundation], mf.mfcreatesensorprofile, mfidl/MFCreateSensorProfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfsensorgroup.lib
req.dll: Mfsensorgroup.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mfsensorgroup.dll
api_name:
 - MFCreateSensorProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateSensorProfile function


## -description


Creates a sensor profile, based on the specified type, index, and optional constraints.


## -parameters




### -param ProfileType [in]

The profile type to create.


### -param ProfileIndex [in, out]

The profile index.


### -param Constraints [in, optional]

Any optional constraints to be put on the profile.


### -param ppProfile [out]

On success, returns a double pointer to the <a href="mf.imfsensorprofile">IMFSensorProfile</a> containing the sensor profile.


## -returns



This function does not return a value.



