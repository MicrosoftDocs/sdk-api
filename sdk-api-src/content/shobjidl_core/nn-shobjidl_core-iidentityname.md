---
UID: NN:shobjidl_core.IIdentityName
title: IIdentityName (shobjidl_core.h)
description: Exposes methods to compare two items to see if they are the same.
helpviewer_keywords: ["IIdentityName","IIdentityName interface [Windows Shell]","IIdentityName interface [Windows Shell]","described","_shell_IIdentityName","shell.IIdentityName","shobjidl_core/IIdentityName"]
old-location: shell\IIdentityName.htm
tech.root: shell
ms.assetid: 9e75141d-b54a-4fe8-9209-40aa7f484d24
ms.date: 12/05/2018
ms.keywords: IIdentityName, IIdentityName interface [Windows Shell], IIdentityName interface [Windows Shell],described, _shell_IIdentityName, shell.IIdentityName, shobjidl_core/IIdentityName
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IIdentityName
 - shobjidl_core/IIdentityName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IIdentityName
---

# IIdentityName interface


## -description

Exposes methods to compare two items to see if they are the same.

## -remarks

This interface provides only the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irelateditem">IRelatedItem</a> interface, from which it inherits.

Shell data sources that present items in virtual locations, such as search results, typically implement this interface as a handler to discover the actual location of an item—to find a folder that contains a file. For example, this interface is used to implement the <b>Open File Location</b> command in Windows Explorer. When the user right-clicks on a file in a set of search results, for example, and then selects <b>Open File Location</b>, the command uses <b>IIdentityName</b> to get the true item and opens a browser on its parent (the file folder) instead of opening the parent of the item (which is where the user already is).

Several controls (the <b>Start</b> button on the taskbar, and the namespace control) use <b>IIdentityName</b> to get the original item and thus avoid duplicate items.

This interface is helpful with aliased ID lists (type <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>), as can be demonstrated using the following two lists.
                

<ol>
<li>[computer][c:][users][pat][desktop][myfile.txt]. This is a file in the user's desktop and is handled by the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> implementation in Windows Vista that handles file systems.</li>
<li>[desktop][myfile.txt]. The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> implementation behind the desktop shows files from the user's desktop, all of the user's desktop, and some special items like the <b>Recycle Bin</b>. When asked to bind through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">IShellFolder::BindToObject</a> using IID IID_IIdentityName, this <b>IShellFolder</b> returns the underlying item, which is the file folder item just above.</li>
</ol>
<div class="alert"><b>Note</b>  To get an instance of this handler use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">IShellFolder::BindToObject</a> with <code>IID_IIdentityItem</code> or use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler">IShellItem::BindToHandler</a> with <code>BHID_SFObject</code>.</div>
<div> </div>