---
UID: NF:shldisp.IShellFolderViewDual3.get_SortColumns
title: IShellFolderViewDual3::get_SortColumns
author: windows-sdk-content
description: Gets the names of the columns used to sort the current folder.
old-location: shell\IShellFolderViewDual3_get_SortColumns.htm
old-project: shell
ms.assetid: 9edad3e2-317f-4ff5-82fb-a816de5d2aa8
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IShellFolderViewDual3 interface [Windows Shell],get_SortColumns method, IShellFolderViewDual3.get_SortColumns, IShellFolderViewDual3::get_SortColumns, _shell_IShellFolderViewDual3_get_SortColumns, get_SortColumns, get_SortColumns method [Windows Shell], get_SortColumns method [Windows Shell],IShellFolderViewDual3 interface, shell.IShellFolderViewDual3_get_SortColumns, shldisp/IShellFolderViewDual3::get_SortColumns
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shldisp.h
api_name:
 - IShellFolderViewDual3.get_SortColumns
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellFolderViewDual3::get_SortColumns


## -description



      Gets the names of the columns used to sort the current folder.


## -parameters




### -param pbstrSortColumns [out]

Type: <b><a href="https://msdn.microsoft.com/library/ms221069(v=VS.85).aspx">BSTR</a>*</b>


          A <b>BSTR</b> that contains the column names.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



