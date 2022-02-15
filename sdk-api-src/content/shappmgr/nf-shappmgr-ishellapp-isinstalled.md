---
UID: NF:shappmgr.IShellApp.IsInstalled
title: IShellApp::IsInstalled (shappmgr.h)
description: Gets a value indicating whether a specified application is currently installed.
helpviewer_keywords: ["IShellApp interface [Windows Shell]","IsInstalled method","IShellApp.IsInstalled","IShellApp::IsInstalled","IsInstalled","IsInstalled method [Windows Shell]","IsInstalled method [Windows Shell]","IShellApp interface","inet_IShellApp_IsInstalled","shappmgr/IShellApp::IsInstalled","shell.IShellApp_IsInstalled"]
old-location: shell\IShellApp_IsInstalled.htm
tech.root: shell
ms.assetid: 338ba632-5749-4850-b982-2247f0d0dcc5
ms.date: 12/05/2018
ms.keywords: IShellApp interface [Windows Shell],IsInstalled method, IShellApp.IsInstalled, IShellApp::IsInstalled, IsInstalled, IsInstalled method [Windows Shell], IsInstalled method [Windows Shell],IShellApp interface, inet_IShellApp_IsInstalled, shappmgr/IShellApp::IsInstalled, shell.IShellApp_IsInstalled
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
 - IShellApp::IsInstalled
 - shappmgr/IShellApp::IsInstalled
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
 - IShellApp.IsInstalled
---

# IShellApp::IsInstalled


## -description

Gets a value indicating whether a specified application is currently installed.



## -returns

Type: <b>HRESULT</b>

This method can return one of these values.

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
The application is installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The application is not installed.

</td>
</tr>
</table>

## -remarks

Application publishers should determine if the application is currently installed and return S_OK if so, or S_FALSE if not.

## -see-also

<a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ishellapp">IShellApp</a>
