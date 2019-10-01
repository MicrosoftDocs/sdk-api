---
UID: NF:shobjidl_core.IUpdateIDList.Update
title: IUpdateIDList::Update (shobjidl_core.h)
author: windows-sdk-content
description: Updates the provided child ITEMIDLIST based on the parameters specified by the provided IBindCtx.
old-location: shell\IUpdateIDList_Update.htm
tech.root: shell
ms.assetid: 29f38464-bd16-4ee9-92b2-6697a3851f55
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUpdateIDList interface [Windows Shell],Update method, IUpdateIDList.Update, IUpdateIDList::Update, Update, Update method [Windows Shell], Update method [Windows Shell],IUpdateIDList interface, _shell_IUpdateIDList_Update, shell.IUpdateIDList_Update, shobjidl_core/IUpdateIDList::Update
ms.topic: method
f1_keywords:
- shobjidl_core/IUpdateIDList.Update
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IUpdateIDList.Update
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdateIDList::Update


## -description


Updates the provided child <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> based on the parameters specified by the provided <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>.


## -parameters




### -param pbc [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

An <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on a bind context object. Used to specify parameters for updating the child <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>. This value can be <b>NULL</b>.


### -param pidlIn [in]

Type: <b>PCUITEMID_CHILD</b>

The child <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>.


### -param ppidlOut [out]

Type: <b>PITEMID_CHILD*</b>

A pointer to the child <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> relative to the parent folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <i>pbc</i> is <b>NULL</b> or does not contain any parameters that apply to the current Shell folder, <i>ppidlOut</i> points to the same <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>  as <i>pidlIn</i>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iupdateidlist">IUpdateIDList</a>
 

 

