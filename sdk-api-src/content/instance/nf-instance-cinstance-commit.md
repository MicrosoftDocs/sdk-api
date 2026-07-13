---
UID: NF:instance.CInstance.Commit
title: CInstance::Commit (instance.h)
description: The Commit method returns the current instance to WMI.
helpviewer_keywords: ["?Commit@CInstance@@QAEJXZ","?Commit@CInstance@@QEAAJXZ","CInstance interface [Windows Management Instrumentation]","Commit method","CInstance.Commit","CInstance::Commit","Commit","Commit method [Windows Management Instrumentation]","Commit method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_commit","instance/CInstance::Commit","wmi.cinstance_commit"]
old-location: wmi\cinstance_commit.htm
tech.root: wmi
ms.assetid: 699dadf9-18b5-4c6d-a5c4-59ea8a85f089
ms.date: 12/05/2018
ms.keywords: ?Commit@CInstance@@QAEJXZ, ?Commit@CInstance@@QEAAJXZ, CInstance interface [Windows Management Instrumentation],Commit method, CInstance.Commit, CInstance::Commit, Commit, Commit method [Windows Management Instrumentation], Commit method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_commit, instance/CInstance::Commit, wmi.cinstance_commit
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
 - CInstance::Commit
 - instance/CInstance::Commit
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
 - CInstance.Commit
 - ?Commit@CInstance@@QAEJXZ
 - ?Commit@CInstance@@QEAAJXZ
---

# CInstance::Commit


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Commit</b> method returns the current instance to WMI.



## -returns

Use the <b>SUCCEEDED</b> or <b>FAILED</b> macro on the returned <b>HRESULT</b> to determine success or failure of the method.

## -remarks

If the client cancels the query, the <b>Commit</b> method returns an error. A provider writer can use this fact to terminate an enumeration.

Also, framework providers should call this method to commit rather than <a href="/windows/desktop/api/provider/nf-provider-provider-commit">Provider::Commit</a>.  <b>Provider::Commit</b> calls <b>CInstance::Release</b> automatically. Smart <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> pointers cannot be used in this case because the smart <b>CInstance</b> pointer would call <b>CInstance::Release</b> in its destructor. If the release has already occurred, an exception will result. Issues of this type are best resolved by allowing the <b>CInstance</b> instance, or a smart pointer to it, to call <b>CInstance::Release</b> when it is appropriate.
