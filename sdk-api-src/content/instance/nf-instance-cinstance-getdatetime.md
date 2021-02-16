---
UID: NF:instance.CInstance.GetDateTime
title: CInstance::GetDateTime (instance.h)
description: The GetDateTime method returns a datetime property.
helpviewer_keywords: ["CInstance interface [Windows Management Instrumentation]","GetDateTime method","CInstance.GetDateTime","CInstance::GetDateTime","GetDateTime","GetDateTime method [Windows Management Instrumentation]","GetDateTime method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_getdatetime","instance/CInstance::GetDateTime","wmi.cinstance_getdatetime"]
old-location: wmi\cinstance_getdatetime.htm
tech.root: wmi
ms.assetid: b7474d1c-4ed9-4669-a0e6-01230a3bf8fa
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],GetDateTime method, CInstance.GetDateTime, CInstance::GetDateTime, GetDateTime, GetDateTime method [Windows Management Instrumentation], GetDateTime method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getdatetime, instance/CInstance::GetDateTime, wmi.cinstance_getdatetime
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
 - CInstance::GetDateTime
 - instance/CInstance::GetDateTime
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
 - CInstance.GetDateTime
---

# CInstance::GetDateTime


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetDateTime</b> method returns a datetime property.

## -parameters

### -param name

Name of the datetime property retrieved.

### -param wbemtime [ref]

Buffer to receive the datetime property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to retrieve a property that is not a datetime value or a property that does not exist. More information is available in the log file, Framework.log.