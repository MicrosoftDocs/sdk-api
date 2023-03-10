---
UID: NF:instance.CInstance.GetEmbeddedObject
title: CInstance::GetEmbeddedObject (instance.h)
description: The GetEmbeddedObject method retrieves a pointer to an embedded CInstance object. The pointer can be used to get and set properties of that embedded object.
helpviewer_keywords: ["?GetEmbeddedObject@CInstance@@QBE_NPBGPAPAV1@PAVMethodContext@@@Z","CInstance interface [Windows Management Instrumentation]","GetEmbeddedObject method","CInstance.GetEmbeddedObject","CInstance::GetEmbeddedObject","GetEmbeddedObject","GetEmbeddedObject method [Windows Management Instrumentation]","GetEmbeddedObject method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_getembeddedobject","instance/CInstance::GetEmbeddedObject","wmi.cinstance_getembeddedobject"]
old-location: wmi\cinstance_getembeddedobject.htm
tech.root: wmi
ms.assetid: e7daf313-d454-4e2c-8a8b-4f1bd9e19c58
ms.date: 12/05/2018
ms.keywords: ?GetEmbeddedObject@CInstance@@QBE_NPBGPAPAV1@PAVMethodContext@@@Z, CInstance interface [Windows Management Instrumentation],GetEmbeddedObject method, CInstance.GetEmbeddedObject, CInstance::GetEmbeddedObject, GetEmbeddedObject, GetEmbeddedObject method [Windows Management Instrumentation], GetEmbeddedObject method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getembeddedobject, instance/CInstance::GetEmbeddedObject, wmi.cinstance_getembeddedobject
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
 - CInstance::GetEmbeddedObject
 - instance/CInstance::GetEmbeddedObject
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
 - CInstance.GetEmbeddedObject
 - ?GetEmbeddedObject@CInstance@@QBE_NPBGPAPAV1@PAVMethodContext@@@Z
---

# CInstance::GetEmbeddedObject


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetEmbeddedObject</b> method retrieves a pointer to an embedded <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> object. The pointer can be used to get and set properties of that embedded object.

## -parameters

### -param name

Name of the <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> property retrieved.

### -param pInstance

Buffer that receives the pointer to the embedded <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> object.

### -param pMethodContext

Additional information communicated to the provider.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to retrieve a property that is not a <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a>-compatible type or a property that does not exist. More information is available in the log file, Framework.log.