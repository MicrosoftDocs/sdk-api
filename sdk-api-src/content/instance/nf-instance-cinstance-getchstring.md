---
UID: NF:instance.CInstance.GetCHString
title: CInstance::GetCHString (instance.h)
description: The GetCHString method retrieves a string property.
helpviewer_keywords: ["?GetCHString@CInstance@@QBE_NPBGAAVCHString@@@Z","?GetCHString@CInstance@@QEBA_NPEBGAEAVCHString@@@Z","CInstance interface [Windows Management Instrumentation]","GetCHString method","CInstance.GetCHString","CInstance::GetCHString","GetCHString","GetCHString method [Windows Management Instrumentation]","GetCHString method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_getchstring","instance/CInstance::GetCHString","wmi.cinstance_getchstring"]
old-location: wmi\cinstance_getchstring.htm
tech.root: wmi
ms.assetid: d9295ba1-19da-41a2-86d1-ec80e18e895b
ms.date: 12/05/2018
ms.keywords: ?GetCHString@CInstance@@QBE_NPBGAAVCHString@@@Z, ?GetCHString@CInstance@@QEBA_NPEBGAEAVCHString@@@Z, CInstance interface [Windows Management Instrumentation],GetCHString method, CInstance.GetCHString, CInstance::GetCHString, GetCHString, GetCHString method [Windows Management Instrumentation], GetCHString method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getchstring, instance/CInstance::GetCHString, wmi.cinstance_getchstring
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
 - CInstance::GetCHString
 - instance/CInstance::GetCHString
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
 - CInstance.GetCHString
 - ?GetCHString@CInstance@@QBE_NPBGAAVCHString@@@Z
 - ?GetCHString@CInstance@@QEBA_NPEBGAEAVCHString@@@Z
---

# CInstance::GetCHString


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetCHString</b> method retrieves a string property.

## -parameters

### -param name

Name of the string property retrieved.

### -param str [ref]

Buffer to receive the string property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to retrieve a nonstring property or a nonexistent property. More information is available in the log file, Framework.log.