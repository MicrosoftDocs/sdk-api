---
UID: NF:instance.CInstance.GetStringArray
title: CInstance::GetStringArray (instance.h)
description: The GetStringArray method retrieves a property that represents an array of strings.
helpviewer_keywords: ["CInstance interface [Windows Management Instrumentation]","GetStringArray method","CInstance.GetStringArray","CInstance::GetStringArray","GetStringArray","GetStringArray method [Windows Management Instrumentation]","GetStringArray method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_getstringarray","instance/CInstance::GetStringArray","wmi.cinstance_getstringarray"]
old-location: wmi\cinstance_getstringarray.htm
tech.root: wmi
ms.assetid: d7fc870a-952e-49a9-87ff-c191e4896511
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],GetStringArray method, CInstance.GetStringArray, CInstance::GetStringArray, GetStringArray, GetStringArray method [Windows Management Instrumentation], GetStringArray method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getstringarray, instance/CInstance::GetStringArray, wmi.cinstance_getstringarray
req.header: instance.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CInstance::GetStringArray
 - instance/CInstance::GetStringArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CInstance.GetStringArray
---

# CInstance::GetStringArray


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetStringArray</b> method retrieves a property that represents an array of strings.

## -parameters

### -param name

Name of the string array property retrieved.

### -param strArray [ref]

Buffer to receive the array of strings.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if the supplied string array type is not valid for the property being returned or an attempt is made to retrieve a nonexistent property. More information is available in the log file, Framework.log.