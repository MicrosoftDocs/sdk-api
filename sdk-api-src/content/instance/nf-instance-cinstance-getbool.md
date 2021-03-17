---
UID: NF:instance.CInstance.Getbool
title: CInstance::Getbool (instance.h)
description: The Getbool method retrieves a Boolean property.
helpviewer_keywords: ["?Getbool@CInstance@@QBE_NPBGAA_N@Z","?Getbool@CInstance@@QEBA_NPEBGAEA_N@Z","CInstance interface [Windows Management Instrumentation]","Getbool method","CInstance.Getbool","CInstance::Getbool","Getbool","Getbool method [Windows Management Instrumentation]","Getbool method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_getbool","instance/CInstance::Getbool","wmi.cinstance_getbool"]
old-location: wmi\cinstance_getbool.htm
tech.root: wmi
ms.assetid: cc8d0c91-03fb-4dc1-86a6-c1117f198181
ms.date: 12/05/2018
ms.keywords: ?Getbool@CInstance@@QBE_NPBGAA_N@Z, ?Getbool@CInstance@@QEBA_NPEBGAEA_N@Z, CInstance interface [Windows Management Instrumentation],Getbool method, CInstance.Getbool, CInstance::Getbool, Getbool, Getbool method [Windows Management Instrumentation], Getbool method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getbool, instance/CInstance::Getbool, wmi.cinstance_getbool
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
 - CInstance::Getbool
 - instance/CInstance::Getbool
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
 - CInstance.Getbool
 - ?Getbool@CInstance@@QBE_NPBGAA_N@Z
 - ?Getbool@CInstance@@QEBA_NPEBGAEA_N@Z
---

# CInstance::Getbool


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Getbool</b> method retrieves a Boolean property.

## -parameters

### -param name

Name of the property retrieved.

### -param b [ref]

Buffer to receive the Boolean property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to retrieve a non-Boolean property or a nonexistent property. More information is available in the log file, Framework.log.