---
UID: NN:shobjidl_core.INewWindowManager
title: INewWindowManager
author: windows-sdk-content
description: Exposes a method that determines whether a window that is launched by another window should be displayed or blocked, allowing control of pop-up windows.
old-location: shell\INewWindowManager.htm
old-project: shell
ms.assetid: 63fbdd29-fe5e-4216-afb3-041320a8c496
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: INewWindowManager, INewWindowManager interface [Windows Shell], INewWindowManager interface [Windows Shell],described, _shell_INewWindowManager, shell.INewWindowManager, shobjidl_core/INewWindowManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - INewWindowManager
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# INewWindowManager interface


## -description


Exposes a method that determines whether a window that is launched by another window should be displayed or blocked, allowing control of pop-up windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INewWindowManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INewWindowManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INewWindowManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0721298f-99c2-463b-8ffa-7527844dcab4">EvaluateNewWindow</a>
</td>
<td align="left" width="63%">
Accepts data about a new window that is attempting to display and determines whether that window should be allowed to open based on the user's preferences.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>INewWindowManager</b> when your application hosts a <a href="_inet_MLang_1">WebBrowser</a> control and you want to include pop-up management functionality.

When you implement <b>INewWindowManager</b>, you can override some or all of the Windows Internet Explorer pop-up blocking logic. To use the default Internet Explorer pop-up blocking logic, implement <a href="https://msdn.microsoft.com/0721298f-99c2-463b-8ffa-7527844dcab4">INewWindowManager::EvaluateNewWindow</a> to return E_FAIL. This instructs the <a href="_inet_MLang_1">WebBrowser</a> control to use the default Internet Explorer implementation. Alternately, the application hosting the WebBrowser control can call <a href="ie.CoInternetSetFeatureEnabled_Function">CoInternetSetFeatureEnabled</a> with the <b>FEATURE_WEBOC_POPUPMANAGEMENT</b> flag for the same result.




## -see-also




<a href="ie.CoInternetSetFeatureEnabled_Function">CoInternetSetFeatureEnabled</a>
 

 

