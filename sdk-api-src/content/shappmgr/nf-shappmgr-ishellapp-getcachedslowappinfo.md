---
UID: NF:shappmgr.IShellApp.GetCachedSlowAppInfo
title: IShellApp::GetCachedSlowAppInfo (shappmgr.h)
description: Returns information to the application that originates from a slow source. Unlike IShellApp::GetSlowAppInfo, this method can return information that has been cached. This method is not applicable to published applications.
helpviewer_keywords: ["GetCachedSlowAppInfo","GetCachedSlowAppInfo method [Windows Shell]","GetCachedSlowAppInfo method [Windows Shell]","IShellApp interface","IShellApp interface [Windows Shell]","GetCachedSlowAppInfo method","IShellApp.GetCachedSlowAppInfo","IShellApp::GetCachedSlowAppInfo","inet_IShellApp_GetCachedSlowAppInfo","shappmgr/IShellApp::GetCachedSlowAppInfo","shell.IShellApp_GetCachedSlowAppInfo"]
old-location: shell\IShellApp_GetCachedSlowAppInfo.htm
tech.root: shell
ms.assetid: 655edc51-0967-4b94-9eef-da213e735e0a
ms.date: 12/05/2018
ms.keywords: GetCachedSlowAppInfo, GetCachedSlowAppInfo method [Windows Shell], GetCachedSlowAppInfo method [Windows Shell],IShellApp interface, IShellApp interface [Windows Shell],GetCachedSlowAppInfo method, IShellApp.GetCachedSlowAppInfo, IShellApp::GetCachedSlowAppInfo, inet_IShellApp_GetCachedSlowAppInfo, shappmgr/IShellApp::GetCachedSlowAppInfo, shell.IShellApp_GetCachedSlowAppInfo
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
 - IShellApp::GetCachedSlowAppInfo
 - shappmgr/IShellApp::GetCachedSlowAppInfo
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
 - IShellApp.GetCachedSlowAppInfo
---

# IShellApp::GetCachedSlowAppInfo


## -description

Returns information to the application that originates from a slow source. Unlike <a href="/windows/desktop/api/shappmgr/nf-shappmgr-ishellapp-getslowappinfo">IShellApp::GetSlowAppInfo</a>, this method can return information that has been cached. This method is not applicable to published applications.

## -parameters

### -param psaid [out]

Type: <b>PSLOWAPPINFO</b>

A pointer to a <a href="/windows/desktop/api/shappmgr/ns-shappmgr-slowappinfo">SLOWAPPINFO</a> structure in which to return application information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Implementations of <a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a> return E_NOTIMPL. This method is used internally by Add/Remove Programs for installed applications.

## -see-also

<a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ishellapp">IShellApp</a>