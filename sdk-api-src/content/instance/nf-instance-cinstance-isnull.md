---
UID: NF:instance.CInstance.IsNull
title: CInstance::IsNull (instance.h)
description: The IsNull method determines if the value of a particular property is NULL.
helpviewer_keywords: ["?IsNull@CInstance@@QBE_NPBG@Z","?IsNull@CInstance@@QEBA_NPEBG@Z","CInstance interface [Windows Management Instrumentation]","IsNull method","CInstance.IsNull","CInstance::IsNull","IsNull","IsNull method [Windows Management Instrumentation]","IsNull method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_isnull","instance/CInstance::IsNull","wmi.cinstance_isnull"]
old-location: wmi\cinstance_isnull.htm
tech.root: wmi
ms.assetid: 54d0135f-f387-43f5-ab5a-aa134141d3b0
ms.date: 12/05/2018
ms.keywords: ?IsNull@CInstance@@QBE_NPBG@Z, ?IsNull@CInstance@@QEBA_NPEBG@Z, CInstance interface [Windows Management Instrumentation],IsNull method, CInstance.IsNull, CInstance::IsNull, IsNull, IsNull method [Windows Management Instrumentation], IsNull method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_isnull, instance/CInstance::IsNull, wmi.cinstance_isnull
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
 - CInstance::IsNull
 - instance/CInstance::IsNull
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
 - CInstance.IsNull
 - ?IsNull@CInstance@@QBE_NPBG@Z
 - ?IsNull@CInstance@@QEBA_NPEBG@Z
---

# CInstance::IsNull


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>IsNull</b> method determines if the value of a particular property is <b>NULL</b>.

## -parameters

### -param name

Name of property that is checked.

## -returns

Returns <b>TRUE</b> if the property specified by <i>name</i> is <b>NULL</b> and <b>FALSE</b> if it is not.