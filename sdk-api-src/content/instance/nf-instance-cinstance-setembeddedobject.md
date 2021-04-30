---
UID: NF:instance.CInstance.SetEmbeddedObject
title: CInstance::SetEmbeddedObject (instance.h)
description: The SetEmbeddedObject method sets an embedded CInstance property.
helpviewer_keywords: ["?SetEmbeddedObject@CInstance@@QAE_NPBGAAV1@@Z","CInstance interface [Windows Management Instrumentation]","SetEmbeddedObject method","CInstance.SetEmbeddedObject","CInstance::SetEmbeddedObject","SetEmbeddedObject","SetEmbeddedObject method [Windows Management Instrumentation]","SetEmbeddedObject method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_setembeddedobject","instance/CInstance::SetEmbeddedObject","wmi.cinstance_setembeddedobject"]
old-location: wmi\cinstance_setembeddedobject.htm
tech.root: wmi
ms.assetid: 64000949-8a3d-47c9-888b-09d520c41e1e
ms.date: 12/05/2018
ms.keywords: ?SetEmbeddedObject@CInstance@@QAE_NPBGAAV1@@Z, CInstance interface [Windows Management Instrumentation],SetEmbeddedObject method, CInstance.SetEmbeddedObject, CInstance::SetEmbeddedObject, SetEmbeddedObject, SetEmbeddedObject method [Windows Management Instrumentation], SetEmbeddedObject method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setembeddedobject, instance/CInstance::SetEmbeddedObject, wmi.cinstance_setembeddedobject
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
 - CInstance::SetEmbeddedObject
 - instance/CInstance::SetEmbeddedObject
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
 - CInstance.SetEmbeddedObject
 - ?SetEmbeddedObject@CInstance@@QAE_NPBGAAV1@@Z
---

# CInstance::SetEmbeddedObject


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetEmbeddedObject</b> method sets an embedded <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> property.

## -parameters

### -param name

Name of the <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> property that is set.

### -param cInstance [ref]

Value assigned to the embedded <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non- <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> property. More information is available in the log file, Framework.log.