---
UID: NF:wbemglue.CWbemProviderGlue.GetNamespaceConnection(LPCWSTR,MethodContext)
title: CWbemProviderGlue::GetNamespaceConnection(LPCWSTR,MethodContext) (wbemglue.h)
description: The GetNameSpaceConnection method is used to retrieve a namespace connection. (overload 1/2)
helpviewer_keywords: ["?GetNamespaceConnection@CWbemProviderGlue@@SAPEAUIWbemServices@@PEBG@Z","?GetNamespaceConnection@CWbemProviderGlue@@SGPAUIWbemServices@@PBG@Z","CWbemProviderGlue interface [Windows Management Instrumentation]","GetNameSpaceConnection method","CWbemProviderGlue.GetNamespaceConnection","CWbemProviderGlue.GetNamespaceConnection(LPCWSTR","MethodContext)","CWbemProviderGlue::GetNameSpaceConnection","CWbemProviderGlue::GetNamespaceConnection","CWbemProviderGlue::GetNamespaceConnection(LPCWSTR","MethodContext)","GetNameSpaceConnection method [Windows Management Instrumentation]","GetNameSpaceConnection method [Windows Management Instrumentation]","CWbemProviderGlue interface","GetNamespaceConnection","_hmm_cwbemproviderglue_getnamespaceconnection","wbemglue/CWbemProviderGlue::GetNameSpaceConnection","wmi.cwbemproviderglue_getnamespaceconnection"]
old-location: wmi\cwbemproviderglue_getnamespaceconnection.htm
tech.root: wmi
ms.assetid: abbc7099-400d-47a0-9673-3d102effa897
ms.date: 12/05/2018
ms.keywords: ?GetNamespaceConnection@CWbemProviderGlue@@SAPEAUIWbemServices@@PEBG@Z, ?GetNamespaceConnection@CWbemProviderGlue@@SGPAUIWbemServices@@PBG@Z, CWbemProviderGlue interface [Windows Management Instrumentation],GetNameSpaceConnection method, CWbemProviderGlue.GetNamespaceConnection, CWbemProviderGlue.GetNamespaceConnection(LPCWSTR,MethodContext), CWbemProviderGlue::GetNameSpaceConnection, CWbemProviderGlue::GetNamespaceConnection, CWbemProviderGlue::GetNamespaceConnection(LPCWSTR,MethodContext), GetNameSpaceConnection method [Windows Management Instrumentation], GetNameSpaceConnection method [Windows Management Instrumentation],CWbemProviderGlue interface, GetNamespaceConnection, _hmm_cwbemproviderglue_getnamespaceconnection, wbemglue/CWbemProviderGlue::GetNameSpaceConnection, wmi.cwbemproviderglue_getnamespaceconnection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CWbemProviderGlue::GetNamespaceConnection
 - wbemglue/CWbemProviderGlue::GetNamespaceConnection
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
 - CWbemProviderGlue.GetNameSpaceConnection
 - ?GetNamespaceConnection@CWbemProviderGlue@@SAPEAUIWbemServices@@PEBG@Z
 - ?GetNamespaceConnection@CWbemProviderGlue@@SGPAUIWbemServices@@PBG@Z
---

# CWbemProviderGlue::GetNamespaceConnection(LPCWSTR,MethodContext)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemglue/nl-wbemglue-cwbemproviderglue">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetNameSpaceConnection</b> method is used to retrieve a namespace connection.

## -parameters

### -param NameSpace

Name of the namespace for which the pointer is returned.

### -param pMethodContext

The method context.

## -returns

Returns a pointer to the namespace if successful, or <b>NULL</b> if not.

## -remarks

The <b>GetNameSpaceConnection</b> method should only be used when the framework functions do not provide the level of control required.
