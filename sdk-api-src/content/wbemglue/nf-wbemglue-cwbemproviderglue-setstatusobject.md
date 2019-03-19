---
UID: NF:wbemglue.CWbemProviderGlue.SetStatusObject
title: CWbemProviderGlue::SetStatusObject (wbemglue.h)
author: windows-sdk-content
description: The SetStatusObject method sets the parameters of a status object used to supply more information when an error occurs. This status object is derived from the Win32_PrivilegesStatus class.
old-location: wmi\cwbemproviderglue_setstatusobject.htm
tech.root: WmiSdk
ms.assetid: 2f094359-66ea-4604-85f8-1f6bc9a81cd1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "?SetStatusObject@CWbemProviderGlue@@SA_NPEAVMethodContext@@PEBG1JPEBUtagSAFEARRAY@@2@Z, ?SetStatusObject@CWbemProviderGlue@@SG_NPAVMethodContext@@PBG1JPBUtagSAFEARRAY@@2@Z, CWbemProviderGlue interface [Windows Management Instrumentation],SetStatusObject method, CWbemProviderGlue.SetStatusObject, CWbemProviderGlue::SetStatusObject, SetStatusObject, SetStatusObject method [Windows Management Instrumentation], SetStatusObject method [Windows Management Instrumentation],CWbemProviderGlue interface, _hmm_cwbemproviderglue_setstatusobject, wbemglue/CWbemProviderGlue::SetStatusObject, wmi.cwbemproviderglue_setstatusobject"
ms.topic: method
req.header: wbemglue.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CWbemProviderGlue.SetStatusObject
 - ?SetStatusObject@CWbemProviderGlue@@SA_NPEAVMethodContext@@PEBG1JPEBUtagSAFEARRAY@@2@Z
 - ?SetStatusObject@CWbemProviderGlue@@SG_NPAVMethodContext@@PBG1JPBUtagSAFEARRAY@@2@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CWbemProviderGlue::SetStatusObject


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/493027c2-e54d-4fad-9e33-98d1ceab8860">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetStatusObject</b> method sets the parameters of a status object used to supply more information when an error occurs. This status object is derived from the <a href="https://msdn.microsoft.com/295ec2bd-7996-4031-8503-d4e869d8368d">Win32_PrivilegesStatus</a> class.


## -parameters




### -param pContext

Pointer to the current context. A context must be provided to prevent deadlocks. Either use the context passed into the provider by <a href="https://msdn.microsoft.com/9566acb0-d7bf-4d3d-b7da-5cfbce150a2c">Provider::EnumerateInstances</a> or <a href="https://msdn.microsoft.com/94d5c8ee-2d61-42af-9a22-cc0df423b245">Provider::ExecQuery</a>, or else obtain it from the instance using <a href="https://msdn.microsoft.com/a2033754-4fd0-405f-9ad9-737eb8931016">CInstance::GetMethodContext</a>. This parameter must not be <b>NULL</b>.


### -param pNamespace

Pointer to the namespace that contains the registration of the <a href="https://msdn.microsoft.com/295ec2bd-7996-4031-8503-d4e869d8368d">Win32_PrivilegesStatus</a> class.


### -param pDescription

Pointer to the value to be put in the <b>Description</b> property of the status object instance.


### -param hr

Value to be put in the <b>StatusCode</b> property of the status object instance.


### -param pPrivilegesNotHeld

This parameter is not currently implemented and must be <b>NULL</b>.


### -param pPrivilegesRequired

Pointer to the value to be put in the <b>PrivilegesRequired</b> property of the status object instance.


## -returns



The method returns <b>TRUE</b> if successful, and <b>FALSE</b> otherwise.



