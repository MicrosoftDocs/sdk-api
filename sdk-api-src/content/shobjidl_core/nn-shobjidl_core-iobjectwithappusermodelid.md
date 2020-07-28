---
UID: NN:shobjidl_core.IObjectWithAppUserModelID
title: IObjectWithAppUserModelID (shobjidl_core.h)
description: Exposes methods that allow implementers of a custom IAssocHandler object to provide access to its explicit Application User Model ID (AppUserModelID).
helpviewer_keywords: ["IObjectWithAppUserModelID","IObjectWithAppUserModelID interface [Windows Shell]","IObjectWithAppUserModelID interface [Windows Shell]","described","_shell_IObjectWithAppUserModelID","shell.IObjectWithAppUserModelID","shobjidl_core/IObjectWithAppUserModelID"]
old-location: shell\IObjectWithAppUserModelID.htm
tech.root: shell
ms.assetid: f5b4e6bf-a5bf-49c5-b343-e9c1ec6c263d
ms.date: 12/05/2018
ms.keywords: IObjectWithAppUserModelID, IObjectWithAppUserModelID interface [Windows Shell], IObjectWithAppUserModelID interface [Windows Shell],described, _shell_IObjectWithAppUserModelID, shell.IObjectWithAppUserModelID, shobjidl_core/IObjectWithAppUserModelID
f1_keywords:
- shobjidl_core/IObjectWithAppUserModelID
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IObjectWithAppUserModelID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectWithAppUserModelID interface


## -description


Exposes methods that allow implementers of a custom <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler">IAssocHandler</a> object to provide access to its explicit Application User Model ID (AppUserModelID). This information is used to determine whether a particular file type can be added to an application's Jump List.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectWithAppUserModelID</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectWithAppUserModelID</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectWithAppUserModelID</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithappusermodelid-getappid">GetAppID</a>
</td>
<td align="left" width="63%">
Retrieves a file type handler's explicit AppUserModelID, if one has been declared.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithappusermodelid-setappid">SetAppID</a>
</td>
<td align="left" width="63%">
Specifies a unique application-defined AppUserModelID that identifies the object as a handler for a specific file type. This method is used by applications that require dynamic AppUserModelIDs.

</td>
</tr>
</table> 


## -remarks



Only file types for which an application is a registered handler appear in that application's Jump List. When an application uses an explicit AppUserModelID to identify itself and the windows and processes that belong to it, that AppUserModelID must also be set in a handler's implemention so that the handler is recognized as being associated with that application. When the application accesses a file such that <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a> is called as a result, an attempt is made to add the file to the <b>Recent</b> or <b>Frequent</b> category, or possibly a custom category, in that application's Jump List. If the application is a registered handler for that file type, identified as such by the handler's AppUserModelID matching the application's AppUserModelID, that file is added to the Jump List. If not, it is filtered and does not appear.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided in Windows. Applications that create custom Shell folders that expose an association handler enumeration needed by the system to determine the files allowed in the application's Jump List should implement their own versions.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
This object is needed only if your application is using explicit AppUserModelIDs. Without an explicit AppUserModelID to expose, there is no need for this object.

<b>IObjectWithAppUserModelID</b> is always used as part of a larger object that uses explicit AppUserModelIDs and wants to expose that information to the system.

The system calls the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithappusermodelid-getappid">IObjectWithAppUserModelID::GetAppID</a> method implemented on a handler to determine whether the application is a registered handler for a file type.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/shell/appids">Application User Model IDs (AppUserModelIDs)</a>



<a href="https://docs.microsoft.com/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>
 

 

