---
UID: NF:shlobj_core.IShellFolderView.Rearrange
title: IShellFolderView::Rearrange (shlobj_core.h)
description: Rearrange may be altered or unavailable.
helpviewer_keywords: ["IShellFolderView interface [Windows Shell]","Rearrange method","IShellFolderView.Rearrange","IShellFolderView::Rearrange","Rearrange","Rearrange method [Windows Shell]","Rearrange method [Windows Shell]","IShellFolderView interface","SHCIDS_ALLFIELDS","SHCIDS_CANONICALONLY","_shell_IShellFolderView_Rearrange","shell.IShellFolderView_Rearrange","shlobj_core/IShellFolderView::Rearrange"]
old-location: shell\IShellFolderView_Rearrange.htm
tech.root: shell
ms.assetid: 9fe955db-dab3-4e53-9c1b-979794052035
ms.date: 12/05/2018
ms.keywords: IShellFolderView interface [Windows Shell],Rearrange method, IShellFolderView.Rearrange, IShellFolderView::Rearrange, Rearrange, Rearrange method [Windows Shell], Rearrange method [Windows Shell],IShellFolderView interface, SHCIDS_ALLFIELDS, SHCIDS_CANONICALONLY, _shell_IShellFolderView_Rearrange, shell.IShellFolderView_Rearrange, shlobj_core/IShellFolderView::Rearrange
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
 - IShellFolderView::Rearrange
 - shlobj_core/IShellFolderView::Rearrange
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
 - IShellFolderView.Rearrange
---

# IShellFolderView::Rearrange


## -description

<p class="CCE_Message">[<b>Rearrange</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getsortcolumns">GetSortColumns</a>.]

Rearranges the items in a view according to a sorting rule.

## -parameters

### -param lParamSort [in]

Type: <b>LPARAM</b>

Specifies how the rearrangement should be performed. 

					

The lower sixteen bits of <i>lParamSort</i> define the sorting rule. Most applications set the sorting rule to the default value of zero, indicating that the items should be sorted by name. The system does not define any other sorting rules. Some folder objects might allow calling applications to use the lower sixteen bits of <i>lParamSort</i> to specify folder-specific sorting rules. The rules and their associated <i>lParamSort</i> values are defined by the folder.

When the system folder view object calls <b>IShellFolderView::Rearrange</b>, the lower sixteen bits of <i>lParamSort</i> are used to specify the column to be used for the arranging.

The upper sixteen bits of <i>lParamSort</i> are used for flags that modify the sorting rule. The system currently defines the following modifier flags.



#### SHCIDS_ALLFIELDS


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0</a>. Arrange all the information contained in the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure, not just the display names. This flag is valid only for folder objects that support the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a> interface. For instance, if the two items are files, the folder should arrange their names, sizes, file times, attributes, and any other information in the structures. If this flag is set, the lower sixteen bits of <i>lParamSort</i> must be zero.



#### SHCIDS_CANONICALONLY


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0</a>. When arranging by name, arrange the system names but not the display names. When this flag is passed, the two items are arranged by whatever criteria the Shell folder determines most efficient, as long as it implements a consistent sort function. This flag cannot be combined with other flags.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<h3><a id="Note_to_Calling_Applications"></a><a id="note_to_calling_applications"></a><a id="NOTE_TO_CALLING_APPLICATIONS"></a>Note to Calling Applications</h3>
Do not set the <b>SHCIDS_ALLFIELDS</b> flag in <i>lParamSort</i> if the folder object does not support <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a>. Doing so might have unpredictable results. If you use the <b>SHCIDS_ALLFIELDS</b> flag, the lower sixteen bits of <i>lParamSort</i> must be set to zero.

<h3><a id="Note_to_Implementers"></a><a id="note_to_implementers"></a><a id="NOTE_TO_IMPLEMENTERS"></a>Note to Implementers</h3>
To extract the sorting rule, use a bitwise AND operator (&amp;) to combine <i>lParamSort</i> with SHCIDS_COLUMNMASK (0X0000FFFF). This operation masks off the upper sixteen bits of <i>lParamSort</i>, including the <b>SHCIDS_ALLFIELDS</b> value.