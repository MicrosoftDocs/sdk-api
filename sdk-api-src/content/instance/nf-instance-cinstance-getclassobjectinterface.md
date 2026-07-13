---
UID: NF:instance.CInstance.GetClassObjectInterface
title: CInstance::GetClassObjectInterface (instance.h)
description: The GetClassObjectInterface method returns an IWbemClassObject interface pointer.
helpviewer_keywords: ["?GetClassObjectInterface@CInstance@@QAEPAUIWbemClassObject@@XZ","?GetClassObjectInterface@CInstance@@QEAAPEAUIWbemClassObject@@XZ","CInstance interface [Windows Management Instrumentation]","GetClassObjectInterface method","CInstance.GetClassObjectInterface","CInstance::GetClassObjectInterface","GetClassObjectInterface","GetClassObjectInterface method [Windows Management Instrumentation]","GetClassObjectInterface method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_getclassobjectinterface","instance/CInstance::GetClassObjectInterface","wmi.cinstance_getclassobjectinterface"]
old-location: wmi\cinstance_getclassobjectinterface.htm
tech.root: wmi
ms.assetid: 2b5e5c14-c036-4ed5-8a47-9a67860e5585
ms.date: 12/05/2018
ms.keywords: ?GetClassObjectInterface@CInstance@@QAEPAUIWbemClassObject@@XZ, ?GetClassObjectInterface@CInstance@@QEAAPEAUIWbemClassObject@@XZ, CInstance interface [Windows Management Instrumentation],GetClassObjectInterface method, CInstance.GetClassObjectInterface, CInstance::GetClassObjectInterface, GetClassObjectInterface, GetClassObjectInterface method [Windows Management Instrumentation], GetClassObjectInterface method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getclassobjectinterface, instance/CInstance::GetClassObjectInterface, wmi.cinstance_getclassobjectinterface
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
 - CInstance::GetClassObjectInterface
 - instance/CInstance::GetClassObjectInterface
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
 - CInstance.GetClassObjectInterface
 - ?GetClassObjectInterface@CInstance@@QAEPAUIWbemClassObject@@XZ
 - ?GetClassObjectInterface@CInstance@@QEAAPEAUIWbemClassObject@@XZ
---

# CInstance::GetClassObjectInterface


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetClassObjectInterface</b> method returns an <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> interface pointer.



## -returns

Returns an <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> interface pointer.

## -remarks

The framework provider will probably never call <b>GetClassObjectInterface</b>, but if it does, it must release the <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> pointer by calling its <b>Release</b> method.
