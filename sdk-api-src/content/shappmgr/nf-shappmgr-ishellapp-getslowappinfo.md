---
UID: NF:shappmgr.IShellApp.GetSlowAppInfo
title: IShellApp::GetSlowAppInfo (shappmgr.h)
description: Returns information to the application that originates from a slow source. This method is not applicable to published applications.
helpviewer_keywords: ["GetSlowAppInfo","GetSlowAppInfo method [Windows Shell]","GetSlowAppInfo method [Windows Shell]","IShellApp interface","IShellApp interface [Windows Shell]","GetSlowAppInfo method","IShellApp.GetSlowAppInfo","IShellApp::GetSlowAppInfo","inet_IShellApp_GetSlowAppInfo","shappmgr/IShellApp::GetSlowAppInfo","shell.IShellApp_GetSlowAppInfo"]
old-location: shell\IShellApp_GetSlowAppInfo.htm
tech.root: shell
ms.assetid: 02f8e527-1c3c-4a2e-bf55-4f33c6a7b822
ms.date: 12/05/2018
ms.keywords: GetSlowAppInfo, GetSlowAppInfo method [Windows Shell], GetSlowAppInfo method [Windows Shell],IShellApp interface, IShellApp interface [Windows Shell],GetSlowAppInfo method, IShellApp.GetSlowAppInfo, IShellApp::GetSlowAppInfo, inet_IShellApp_GetSlowAppInfo, shappmgr/IShellApp::GetSlowAppInfo, shell.IShellApp_GetSlowAppInfo
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellApp::GetSlowAppInfo
 - shappmgr/IShellApp::GetSlowAppInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellApp.GetSlowAppInfo
---

# IShellApp::GetSlowAppInfo


## -description

Returns information to the application that originates from a slow source. This method is not applicable to published applications.

## -parameters

### -param psaid [out]

Type: <b>PSLOWAPPINFO</b>

A pointer to a <a href="/windows/desktop/api/shappmgr/ns-shappmgr-slowappinfo">SLOWAPPINFO</a> structure in which to return application information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Implementations of <a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a> should return E_NOTIMPL. This method is used internally by Add/Remove Programs for installed applications.

## -see-also

<a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ishellapp">IShellApp</a>