---
UID: NF:shappmgr.IShellApp.GetPossibleActions
title: IShellApp::GetPossibleActions (shappmgr.h)
description: Gets a bitmask of management actions allowed for an application.
helpviewer_keywords: ["GetPossibleActions","GetPossibleActions method [Windows Shell]","GetPossibleActions method [Windows Shell]","IShellApp interface","IShellApp interface [Windows Shell]","GetPossibleActions method","IShellApp.GetPossibleActions","IShellApp::GetPossibleActions","inet_IShellApp_GetPossibleActions","shappmgr/IShellApp::GetPossibleActions","shell.IShellApp_GetPossibleActions"]
old-location: shell\IShellApp_GetPossibleActions.htm
tech.root: shell
ms.assetid: e2cdff59-1339-4d00-9bbc-e34e773da1c2
ms.date: 12/05/2018
ms.keywords: GetPossibleActions, GetPossibleActions method [Windows Shell], GetPossibleActions method [Windows Shell],IShellApp interface, IShellApp interface [Windows Shell],GetPossibleActions method, IShellApp.GetPossibleActions, IShellApp::GetPossibleActions, inet_IShellApp_GetPossibleActions, shappmgr/IShellApp::GetPossibleActions, shell.IShellApp_GetPossibleActions
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
 - IShellApp::GetPossibleActions
 - shappmgr/IShellApp::GetPossibleActions
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
 - IShellApp.GetPossibleActions
---

# IShellApp::GetPossibleActions


## -description

Gets a bitmask of management actions allowed for an application.

## -parameters

### -param pdwActions [out]

Type: <b>DWORD*</b>

A pointer to a variable of type <b>DWORD</b> that returns the bitmask of supported actions. The bit flags are described in <a href="/windows/desktop/api/shappmgr/ne-shappmgr-appactionflags">APPACTIONFLAGS</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Of the set of <a href="/windows/desktop/api/shappmgr/ne-shappmgr-appactionflags">APPACTIONFLAGS</a> bitmasks, Add/Remove Programs only recognizes APPACTION_INSTALL and APPACTION_ADDLATER.

## -see-also

<a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ishellapp">IShellApp</a>