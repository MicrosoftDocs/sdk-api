---
UID: NN:shobjidl_core.IApplicationDestinations
title: IApplicationDestinations (shobjidl_core.h)
description: Exposes methods that allow an application to remove one or all destinations from the Recent or Frequent categories in a Jump List.
helpviewer_keywords: ["IApplicationDestinations","IApplicationDestinations interface [Windows Shell]","IApplicationDestinations interface [Windows Shell]","described","_shell_IApplicationDestinations","shell.IApplicationDestinations","shobjidl_core/IApplicationDestinations"]
old-location: shell\IApplicationDestinations.htm
tech.root: shell
ms.assetid: d425eb2c-75c7-431e-9607-11ea2e092178
ms.date: 12/05/2018
ms.keywords: IApplicationDestinations, IApplicationDestinations interface [Windows Shell], IApplicationDestinations interface [Windows Shell],described, _shell_IApplicationDestinations, shell.IApplicationDestinations, shobjidl_core/IApplicationDestinations
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IApplicationDestinations
 - shobjidl_core/IApplicationDestinations
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
 - IApplicationDestinations
---

# IApplicationDestinations interface


## -description

Exposes methods that allow an application to remove one or all destinations from the <b>Recent</b> or <b>Frequent</b> categories in a Jump List.

## -inheritance

The <b>IApplicationDestinations</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IApplicationDestinations</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided in Windows as CLSID_ApplicationDestinations. This interface is not implemented by third parties.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
An application calls the methods of this interface when it wants to remove items from a Jump List's automatically generated destinations. These destinations, found in the <b>Recent</b> or <b>Frequent</b> categories, are generated through calls to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a>, either explicitly or by the system when a file is opened through Windows Explorer or the common file dialog is used to open, save, or create a file.



An application should call <b>IApplicationDestinations</b> methods in the following situations:
                
<ul>
<li>When the application is uninstalled.</li>
<li>When the user clears history.</li>
<li>When the user disables destination tracking in the application's Settings or Options pages.</li>
<li>When the user deletes the destination from within the application. This is particularly important in the case of a destination that is not a file. In the case of non-file destinations—generally, though not always, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> items—it is the application's responsibility to remove the destination from the list when it detects that it no longer exists.</li>
</ul>


If the user turns off usage tracking in the application's privacy setting, the application is responsible for clearing the existing data and also stopping the system from collecting usage data on that item in the future. This is done by setting the NoRecentDocs value in all of the application's file type registrations. See <a href="/windows/desktop/api/shlwapi/ne-shlwapi-filetypeattributeflags">FTA_NoRecentDocs</a> for more information.

<b>IApplicationDestinations</b> methods are used only with the automatically generated <b>Recent</b> or <b>Frequent</b> categories. They do not remove items that the user has pinned to the Jump List. Those items cannot be removed programmatically; only the user can remove them. These methods also have no effect on <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist">custom categories</a> or the task list.

## -see-also

<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>
