---
UID: NF:wbemglue.CWbemProviderGlue.GetEmptyInstance(LPCWSTR,CInstance,LPCWSTR)
title: CWbemProviderGlue::GetEmptyInstance(LPCWSTR,CInstance,LPCWSTR)
author: windows-sdk-content
description: The GetEmptyInstance method retrieves a single unpopulated instance of the specified class.
old-location: wmi\cwbemproviderglue_getemptyinstance_lpcwstr_cinstance___lpcwstr_.htm
tech.root: WmiSdk
ms.assetid: 15b34445-769f-48dd-9e64-1820ab43aeda
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CWbemProviderGlue interface [Windows Management Instrumentation],GetEmptyInstance method, CWbemProviderGlue.GetEmptyInstance, CWbemProviderGlue.GetEmptyInstance(LPCWSTR,CInstance,LPCWSTR), CWbemProviderGlue::GetEmptyInstance, CWbemProviderGlue::GetEmptyInstance(LPCWSTR,CInstance**,LPCWSTR), CWbemProviderGlue::GetEmptyInstance(LPCWSTR,CInstance,LPCWSTR), GetEmptyInstance, GetEmptyInstance method [Windows Management Instrumentation], GetEmptyInstance method [Windows Management Instrumentation],CWbemProviderGlue interface, wbemglue/CWbemProviderGlue::GetEmptyInstance, wmi.cwbemproviderglue_getemptyinstance_lpcwstr_cinstance___lpcwstr_
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CWbemProviderGlue.GetEmptyInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wbemglue.h
: 
- CWbemProviderGlue.GetEmptyInstance
: 
---

# CWbemProviderGlue::GetEmptyInstance(LPCWSTR,CInstance,LPCWSTR)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/493027c2-e54d-4fad-9e33-98d1ceab8860">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetEmptyInstance</b> method retrieves a single unpopulated instance of the specified class.


## -parameters




### -param pszClassName

Name of the class whose instance is to be returned.


### -param ppInstance

Pointer to an instance of the <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class used to store the new instance. This pointer must be released by the framework provider calling <b>GetEmptyInstance</b>.


### -param pszNamespace

Namespace of the class name specified by <i>pszClassName</i>. This parameter can be <b>NULL</b> to indicate the default namespace, which is root\cimv2.


## -returns



Returns <b>WBEM_S_NO_ERROR</b> if the operation was successful, <b>WBEM_E_OUT_OF_MEMORY</b> if the operation failed due to lack of memory, or any other <b>HRESULT</b> error code.




## -remarks



The framework provider pass the name of the provider to <b>GetEmptyInstance</b>, which returns an empty instance. A common use of this method is to populate an embedded object property. This method is used in conjunction with <a href="https://msdn.microsoft.com/64000949-8a3d-47c9-888b-09d520c41e1e">CInstance::SetEmbeddedObject</a>.

The second function prototype is not recommended. It is provided only to support existing code.



