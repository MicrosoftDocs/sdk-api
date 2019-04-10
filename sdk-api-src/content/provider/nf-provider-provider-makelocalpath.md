---
UID: NF:provider.Provider.MakeLocalPath
title: Provider::MakeLocalPath (provider.h)
author: windows-sdk-content
description: The MakeLocalPath method builds a full instance path from a relative path.
old-location: wmi\provider_makelocalpath.htm
tech.root: WmiSdk
ms.assetid: 8a2476c0-73c0-4a95-8973-e6da451116af
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MakeLocalPath, MakeLocalPath method [Windows Management Instrumentation], MakeLocalPath method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],MakeLocalPath method, Provider.MakeLocalPath, Provider::MakeLocalPath, _hmm_provider_makelocalpath, provider/Provider::MakeLocalPath, wmi.provider_makelocalpath
ms.topic: method
req.header: provider.h
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
 - Provider.MakeLocalPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Provider::MakeLocalPath


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/d8a7c433-7e6a-45cc-914f-a15a3688c7aa">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>MakeLocalPath</b> method builds a full instance path from a relative path.


## -parameters




### -param strRelPath [ref]

Relative path used to build the full path.


## -returns



Returns the full path in <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> format.




## -remarks



Consider using <a href="https://msdn.microsoft.com/c419205f-d07d-4887-8e36-ccde37c2351f">Provider::GetLocalInstancePath</a> before using this method.



