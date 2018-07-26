---
UID: NF:shobjidl_core.IFolderView2.SetSortColumns
title: IFolderView2::SetSortColumns
author: windows-sdk-content
description: Sets and sorts the view by the given sort columns.
old-location: shell\IFolderView2_SetSortColumns.htm
old-project: shell
ms.assetid: 54dfac6b-8355-4064-9f54-4172975b8028
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IFolderView2 interface [Windows Shell],SetSortColumns method, IFolderView2.SetSortColumns, IFolderView2::SetSortColumns, SetSortColumns, SetSortColumns method [Windows Shell], SetSortColumns method [Windows Shell],IFolderView2 interface, _shell_IFolderView2_SetSortColumns, shell.IFolderView2_SetSortColumns, shobjidl_core/IFolderView2::SetSortColumns
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFolderView2.SetSortColumns
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFolderView2::SetSortColumns


## -description


Sets and sorts the view by the given sort columns.  


## -parameters




### -param rgSortColumns [in]

Type: <b>const <a href="https://msdn.microsoft.com/3ca4c318-6462-4e22-813c-ef7b3ef03230">SORTCOLUMN</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/3ca4c318-6462-4e22-813c-ef7b3ef03230">SORTCOLUMN</a> structure. The size of this structure is determined by <i>cColumns</i>.


### -param cColumns [in]

Type: <b>int</b>

The count of columns to sort by.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



