---
UID: NF:shobjidl_core.INewWindowManager.EvaluateNewWindow
title: INewWindowManager::EvaluateNewWindow (shobjidl_core.h)
description: Accepts data about a new window that is attempting to display and determines whether that window should be allowed to open based on the user's preferences.
helpviewer_keywords: ["EvaluateNewWindow","EvaluateNewWindow method [Windows Shell]","EvaluateNewWindow method [Windows Shell]","INewWindowManager interface","INewWindowManager interface [Windows Shell]","EvaluateNewWindow method","INewWindowManager.EvaluateNewWindow","INewWindowManager::EvaluateNewWindow","_shell_INewWindowManager_EvaluateNewWindow","shell.INewWindowManager_EvaluateNewWindow","shobjidl_core/INewWindowManager::EvaluateNewWindow"]
old-location: shell\INewWindowManager_EvaluateNewWindow.htm
tech.root: shell
ms.assetid: 0721298f-99c2-463b-8ffa-7527844dcab4
ms.date: 12/05/2018
ms.keywords: EvaluateNewWindow, EvaluateNewWindow method [Windows Shell], EvaluateNewWindow method [Windows Shell],INewWindowManager interface, INewWindowManager interface [Windows Shell],EvaluateNewWindow method, INewWindowManager.EvaluateNewWindow, INewWindowManager::EvaluateNewWindow, _shell_INewWindowManager_EvaluateNewWindow, shell.INewWindowManager_EvaluateNewWindow, shobjidl_core/INewWindowManager::EvaluateNewWindow
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
 - INewWindowManager::EvaluateNewWindow
 - shobjidl_core/INewWindowManager::EvaluateNewWindow
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
 - INewWindowManager.EvaluateNewWindow
---

# INewWindowManager::EvaluateNewWindow


## -description

Accepts data about a new window that is attempting to display and determines whether that window should be allowed to open based on the user's preferences.

## -parameters

### -param pszUrl [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the URL of the content that will be displayed in the new window.

### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the name of the new window. This parameter can be <b>NULL</b>.

### -param pszUrlContext [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the URL that has issued the command to open the new window.

### -param pszFeatures [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the feature string for the new window. This value can be <b>NULL</b>.

### -param fReplace [in]

Type: <b>BOOL</b>

A boolean value used when the new content specified in <i>pszUrl</i> is loaded into the existing window instead of creating a new one. <b>TRUE</b> if the new document should replace the current document in the history list; <b>FALSE</b> if the new document should be given a new entry.

### -param dwFlags [in]

Type: <b>DWORD</b>

A flag or flags from the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nwmf">NWMF</a> enumeration that provide situational information about the call to open the new window. This value can be 0 if no flags are needed.

### -param dwUserActionTime [in]

Type: <b>DWORD</b>

The tick count when the last user action occurred. To find out how long ago the action occurred, call <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount">GetTickCount</a> and compare the result with the value in this parameter.

## -returns

Type: <b>HRESULT</b>

Returns standard error codes, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Allow display of the window.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Block display of the window.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
When you implement <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewwindowmanager">INewWindowManager</a> for a hosted <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85)">WebBrowser</a> control, this value instructs the WebBrowser control to use the default implementation.

</td>
</tr>
</table>