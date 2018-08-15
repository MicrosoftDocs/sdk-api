---
UID: NF:instance.CInstance.GetClassObjectInterface
title: CInstance::GetClassObjectInterface
author: windows-sdk-content
description: The GetClassObjectInterface method returns an IWbemClassObject interface pointer.
old-location: wmi\cinstance_getclassobjectinterface.htm
old-project: WmiSdk
ms.assetid: 2b5e5c14-c036-4ed5-8a47-9a67860e5585
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: "?GetClassObjectInterface@CInstance@@QAEPAUIWbemClassObject@@XZ, ?GetClassObjectInterface@CInstance@@QEAAPEAUIWbemClassObject@@XZ, CInstance interface [Windows Management Instrumentation],GetClassObjectInterface method, CInstance.GetClassObjectInterface, CInstance::GetClassObjectInterface, GetClassObjectInterface, GetClassObjectInterface method [Windows Management Instrumentation], GetClassObjectInterface method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getclassobjectinterface, instance/CInstance::GetClassObjectInterface, wmi.cinstance_getclassobjectinterface"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: instance.h
req.include-header: FwCommon.h
req.redist: 
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
tech.root: 
req.typenames: TrustLevel
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CInstance.GetClassObjectInterface
 - ?GetClassObjectInterface@CInstance@@QAEPAUIWbemClassObject@@XZ
 - ?GetClassObjectInterface@CInstance@@QEAAPEAUIWbemClassObject@@XZ
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: GDI+ 1.1
---

# CInstance::GetClassObjectInterface


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetClassObjectInterface</b> method returns an <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> interface pointer.


## -parameters






## -returns



Returns an <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> interface pointer.




## -remarks



The framework provider will probably never call <b>GetClassObjectInterface</b>, but if it does, it must release the <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> pointer by calling its <b>Release</b> method.



