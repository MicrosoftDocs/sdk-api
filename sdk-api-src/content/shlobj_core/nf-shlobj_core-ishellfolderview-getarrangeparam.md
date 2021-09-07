---
UID: NF:shlobj_core.IShellFolderView.GetArrangeParam
title: IShellFolderView::GetArrangeParam (shlobj_core.h)
description: Gets the arrangement parameter of the view, which is how the view has been sorted.
helpviewer_keywords: ["GetArrangeParam","GetArrangeParam method [Windows Shell]","GetArrangeParam method [Windows Shell]","IShellFolderView interface","IShellFolderView interface [Windows Shell]","GetArrangeParam method","IShellFolderView.GetArrangeParam","IShellFolderView::GetArrangeParam","SHCIDS_ALLFIELDS","SHCIDS_CANONICALONLY","_shell_IShellFolderView_GetArrangeParam","shell.IShellFolderView_GetArrangeParam","shlobj_core/IShellFolderView::GetArrangeParam"]
old-location: shell\IShellFolderView_GetArrangeParam.htm
tech.root: shell
ms.assetid: 15eda2f2-6956-47c1-be08-3ca2f292578e
ms.date: 12/05/2018
ms.keywords: GetArrangeParam, GetArrangeParam method [Windows Shell], GetArrangeParam method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],GetArrangeParam method, IShellFolderView.GetArrangeParam, IShellFolderView::GetArrangeParam, SHCIDS_ALLFIELDS, SHCIDS_CANONICALONLY, _shell_IShellFolderView_GetArrangeParam, shell.IShellFolderView_GetArrangeParam, shlobj_core/IShellFolderView::GetArrangeParam
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IShellFolderView::GetArrangeParam
 - shlobj_core/IShellFolderView::GetArrangeParam
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shlobj_core.h
api_name:
 - IShellFolderView.GetArrangeParam
---

# IShellFolderView::GetArrangeParam


## -description

Gets the arrangement parameter of the view, which is how the view has been sorted.
        
            
<div class="alert"><b>Note</b>  This method is deprecated as of Windows Vista. It might be altered or unavailable in subsequent versions of Windows. We recommend that you use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getsortcolumns">IFolderView2::GetSortColumns</a> instead.</div><div> </div>

## -parameters

### -param plParamSort [out]

Type: <b>LPARAM*</b>

The lower sixteen bits of <i>plParamSort</i> define the sorting rule. Most applications set the sorting rule to the default value of zero, indicating that the items should be sorted by name. The system does not define any other sorting rules. Some folder objects might allow calling applications to use the lower sixteen bits of <i>plParamSort</i> to specify folder-specific sorting rules. The rules and their associated <i>plParamSort</i> values are defined by the folder.
    
    					

When the system folder view object calls <b>IShellFolderView::GetArrangeParam</b>, the lower sixteen bits of <i>plParamSort</i> are used to specify the column to be used for the arranging.

The upper sixteen bits of <i>plParamSort</i> are used for flags that modify the sorting rule. The system currently defines the following modifier flags.



#### SHCIDS_ALLFIELDS


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0</a>. Arrange all the information contained in the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure, not just the display names. This flag is valid only for folder objects that support the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a> interface. For instance, if the two items are files, the folder arranges their names, sizes, file times, attributes, and any other information in the structures. If this flag is set, the lower sixteen bits of <i>plParamSort</i> must be zero.



#### SHCIDS_CANONICALONLY


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0</a>. When arranging by name, arrange the system names but not the display names. When this flag is passed, the two items are arranged by whatever criteria the Shell folder determines most efficient, as long as it implements a consistent sort function. This flag cannot be combined with other flags.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.