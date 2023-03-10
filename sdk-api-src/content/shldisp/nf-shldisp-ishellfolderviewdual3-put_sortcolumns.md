---
UID: NF:shldisp.IShellFolderViewDual3.put_SortColumns
title: IShellFolderViewDual3::put_SortColumns (shldisp.h)
description: Sets the names of the columns to be sorted.
helpviewer_keywords: ["IShellFolderViewDual3 interface [Windows Shell]","put_SortColumns method","IShellFolderViewDual3.put_SortColumns","IShellFolderViewDual3::put_SortColumns","_shell_IShellFolderViewDual3_put_SortColumns","put_SortColumns","put_SortColumns method [Windows Shell]","put_SortColumns method [Windows Shell]","IShellFolderViewDual3 interface","shell.IShellFolderViewDual3_put_SortColumns","shldisp/IShellFolderViewDual3::put_SortColumns"]
old-location: shell\IShellFolderViewDual3_put_SortColumns.htm
tech.root: shell
ms.assetid: cd61c44e-1612-48e3-9230-1a3a4667ece6
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual3 interface [Windows Shell],put_SortColumns method, IShellFolderViewDual3.put_SortColumns, IShellFolderViewDual3::put_SortColumns, _shell_IShellFolderViewDual3_put_SortColumns, put_SortColumns, put_SortColumns method [Windows Shell], put_SortColumns method [Windows Shell],IShellFolderViewDual3 interface, shell.IShellFolderViewDual3_put_SortColumns, shldisp/IShellFolderViewDual3::put_SortColumns
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
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
 - IShellFolderViewDual3::put_SortColumns
 - shldisp/IShellFolderViewDual3::put_SortColumns
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shldisp.h
api_name:
 - IShellFolderViewDual3.put_SortColumns
---

# IShellFolderViewDual3::put_SortColumns


## -description

Sets the names of the columns to be sorted.

## -parameters

### -param bstrSortColumns [in]

Type: <b><a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a></b>

The <b>BSTR</b> that contains the names of the columns to be sorted for the current folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.