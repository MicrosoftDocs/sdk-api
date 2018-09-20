---
UID: NF:shlobj_core.IShellFolderView.GetArrangeParam
title: IShellFolderView::GetArrangeParam
author: windows-sdk-content
description: Gets the arrangement parameter of the view, which is how the view has been sorted.
old-location: shell\IShellFolderView_GetArrangeParam.htm
tech.root: shell
ms.assetid: 15eda2f2-6956-47c1-be08-3ca2f292578e
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: GetArrangeParam, GetArrangeParam method [Windows Shell], GetArrangeParam method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],GetArrangeParam method, IShellFolderView.GetArrangeParam, IShellFolderView::GetArrangeParam, SHCIDS_ALLFIELDS, SHCIDS_CANONICALONLY, _shell_IShellFolderView_GetArrangeParam, shell.IShellFolderView_GetArrangeParam, shlobj_core/IShellFolderView::GetArrangeParam
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shlobj_core.h
api_name:
 - IShellFolderView.GetArrangeParam
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderView::GetArrangeParam


## -description


Gets the arrangement parameter of the view, which is how the view has been sorted.
        
            
<div class="alert"><b>Note</b>  This method is deprecated as of Windows Vista. It might be altered or unavailable in subsequent versions of Windows. We recommend that you use <a href="https://msdn.microsoft.com/33d005bd-3ea0-42d0-ae87-417fb7c087d4">IFolderView2::GetSortColumns</a> instead.</div><div> </div>

## -parameters




### -param plParamSort [out]

Type: <b>LPARAM*</b>

The lower sixteen bits of <i>plParamSort</i> define the sorting rule. Most applications set the sorting rule to the default value of zero, indicating that the items should be sorted by name. The system does not define any other sorting rules. Some folder objects might allow calling applications to use the lower sixteen bits of <i>plParamSort</i> to specify folder-specific sorting rules. The rules and their associated <i>plParamSort</i> values are defined by the folder.
    
    					

When the system folder view object calls <b>IShellFolderView::GetArrangeParam</b>, the lower sixteen bits of <i>plParamSort</i> are used to specify the column to be used for the arranging.

The upper sixteen bits of <i>plParamSort</i> are used for flags that modify the sorting rule. The system currently defines the following modifier flags.



#### SHCIDS_ALLFIELDS


<a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. Arrange all the information contained in the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure, not just the display names. This flag is valid only for folder objects that support the <a href="https://msdn.microsoft.com/9b008034-3576-429e-b67c-e2222592ca46">IShellFolder2</a> interface. For instance, if the two items are files, the folder arranges their names, sizes, file times, attributes, and any other information in the structures. If this flag is set, the lower sixteen bits of <i>plParamSort</i> must be zero.



#### SHCIDS_CANONICALONLY


<a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. When arranging by name, arrange the system names but not the display names. When this flag is passed, the two items are arranged by whatever criteria the Shell folder determines most efficient, as long as it implements a consistent sort function. This flag cannot be combined with other flags.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



