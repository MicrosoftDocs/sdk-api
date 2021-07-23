---
UID: NN:shobjidl_core.INewWindowManager
title: INewWindowManager (shobjidl_core.h)
description: Exposes a method that determines whether a window that is launched by another window should be displayed or blocked, allowing control of pop-up windows.
helpviewer_keywords: ["INewWindowManager","INewWindowManager interface [Windows Shell]","INewWindowManager interface [Windows Shell]","described","_shell_INewWindowManager","shell.INewWindowManager","shobjidl_core/INewWindowManager"]
old-location: shell\INewWindowManager.htm
tech.root: shell
ms.assetid: 63fbdd29-fe5e-4216-afb3-041320a8c496
ms.date: 12/05/2018
ms.keywords: INewWindowManager, INewWindowManager interface [Windows Shell], INewWindowManager interface [Windows Shell],described, _shell_INewWindowManager, shell.INewWindowManager, shobjidl_core/INewWindowManager
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - INewWindowManager
 - shobjidl_core/INewWindowManager
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
 - INewWindowManager
---

# INewWindowManager interface


## -description

Exposes a method that determines whether a window that is launched by another window should be displayed or blocked, allowing control of pop-up windows.

## -inheritance

The <b>INewWindowManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INewWindowManager</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>INewWindowManager</b> when your application hosts a <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85)">WebBrowser</a> control and you want to include pop-up management functionality.

When you implement <b>INewWindowManager</b>, you can override some or all of the Windows Internet Explorer pop-up blocking logic. To use the default Internet Explorer pop-up blocking logic, implement <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow">INewWindowManager::EvaluateNewWindow</a> to return E_FAIL. This instructs the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85)">WebBrowser</a> control to use the default Internet Explorer implementation. Alternately, the application hosting the WebBrowser control can call <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537168(v=vs.85)">CoInternetSetFeatureEnabled</a> with the <b>FEATURE_WEBOC_POPUPMANAGEMENT</b> flag for the same result.

## -see-also

<a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537168(v=vs.85)">CoInternetSetFeatureEnabled</a>
