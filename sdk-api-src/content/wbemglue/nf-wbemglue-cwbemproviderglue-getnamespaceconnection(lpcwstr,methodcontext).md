---
UID: NF:wbemglue.CWbemProviderGlue.GetNamespaceConnection(LPCWSTR,MethodContext)
title: CWbemProviderGlue::GetNamespaceConnection(LPCWSTR,MethodContext)
author: windows-sdk-content
description: The GetNameSpaceConnection method is used to retrieve a namespace connection.
old-location: wmi\cwbemproviderglue_getnamespaceconnection.htm
old-project: WmiSdk
ms.assetid: abbc7099-400d-47a0-9673-3d102effa897
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: "?GetNamespaceConnection@CWbemProviderGlue@@SAPEAUIWbemServices@@PEBG@Z, ?GetNamespaceConnection@CWbemProviderGlue@@SGPAUIWbemServices@@PBG@Z, CWbemProviderGlue interface [Windows Management Instrumentation],GetNameSpaceConnection method, CWbemProviderGlue.GetNamespaceConnection, CWbemProviderGlue.GetNamespaceConnection(LPCWSTR,MethodContext), CWbemProviderGlue::GetNameSpaceConnection, CWbemProviderGlue::GetNamespaceConnection, CWbemProviderGlue::GetNamespaceConnection(LPCWSTR,MethodContext), GetNameSpaceConnection method [Windows Management Instrumentation], GetNameSpaceConnection method [Windows Management Instrumentation],CWbemProviderGlue interface, GetNamespaceConnection, _hmm_cwbemproviderglue_getnamespaceconnection, wbemglue/CWbemProviderGlue::GetNameSpaceConnection, wmi.cwbemproviderglue_getnamespaceconnection"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CWbemProviderGlue.GetNameSpaceConnection
 - ?GetNamespaceConnection@CWbemProviderGlue@@SAPEAUIWbemServices@@PEBG@Z
 - ?GetNamespaceConnection@CWbemProviderGlue@@SGPAUIWbemServices@@PBG@Z
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CWbemProviderGlue::GetNamespaceConnection(LPCWSTR,MethodContext)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/493027c2-e54d-4fad-9e33-98d1ceab8860">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetNameSpaceConnection</b> method is used to retrieve a namespace connection.


## -parameters




### -param NameSpace




### -param pMethodContext






#### - namespace

Name of the namespace for which the pointer is returned.


## -returns



Returns a pointer to the namespace if successful, or <b>NULL</b> if not.




## -remarks



The <b>GetNameSpaceConnection</b> method should only be used when the framework functions do not provide the level of control required.



