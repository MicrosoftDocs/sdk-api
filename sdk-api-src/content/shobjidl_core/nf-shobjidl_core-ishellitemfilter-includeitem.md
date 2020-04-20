---
UID: NF:shobjidl_core.IShellItemFilter.IncludeItem
title: IShellItemFilter::IncludeItem (shobjidl_core.h)
description: Sets a given Shell item status to inclusion in the view.helpviewer_keywords: ["IShellItemFilter interface [Windows Shell]","IncludeItem method","IShellItemFilter.IncludeItem","IShellItemFilter::IncludeItem","IncludeItem","IncludeItem method [Windows Shell]","IncludeItem method [Windows Shell]","IShellItemFilter interface","_shell_IShellItemFilter_IncludeItem","shell.IShellItemFilter_IncludeItem","shobjidl_core/IShellItemFilter::IncludeItem"]
old-location: shell\IShellItemFilter_IncludeItem.htm
tech.root: shell
ms.assetid: 39ec171e-24a0-40ff-b199-36b5a2809164
ms.date: 12/05/2018
ms.keywords: IShellItemFilter interface [Windows Shell],IncludeItem method, IShellItemFilter.IncludeItem, IShellItemFilter::IncludeItem, IncludeItem, IncludeItem method [Windows Shell], IncludeItem method [Windows Shell],IShellItemFilter interface, _shell_IShellItemFilter_IncludeItem, shell.IShellItemFilter_IncludeItem, shobjidl_core/IShellItemFilter::IncludeItem
f1_keywords:
- shobjidl_core/IShellItemFilter.IncludeItem
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IShellItemFilter.IncludeItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellItemFilter::IncludeItem


## -description


Sets a given <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">Shell item</a> status to inclusion in the view.


## -parameters




### -param psi [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">Shell item</a> that is to be included in the view.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The host calls this method for each item in the folder. Returns S_OK to have the item enumerated for inclusion in the view. Returns S_FALSE to prevent the item from being enumerated for inclusion in the view.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemfilter">IShellItemFilter</a>
 

 

