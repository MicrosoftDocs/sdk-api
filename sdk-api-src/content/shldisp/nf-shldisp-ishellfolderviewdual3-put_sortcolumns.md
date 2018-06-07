---
UID: NF:shldisp.IShellFolderViewDual3.put_SortColumns
title: IShellFolderViewDual3::put_SortColumns
author: windows-sdk-content
description: Sets the names of the columns to be sorted.
old-location: shell\IShellFolderViewDual3_put_SortColumns.htm
old-project: shell
ms.assetid: cd61c44e-1612-48e3-9230-1a3a4667ece6
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IShellFolderViewDual3 interface [Windows Shell],put_SortColumns method, IShellFolderViewDual3.put_SortColumns, IShellFolderViewDual3::put_SortColumns, _shell_IShellFolderViewDual3_put_SortColumns, put_SortColumns, put_SortColumns method [Windows Shell], put_SortColumns method [Windows Shell],IShellFolderViewDual3 interface, shell.IShellFolderViewDual3_put_SortColumns, shldisp/IShellFolderViewDual3::put_SortColumns
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
 - IShellFolderViewDual3.put_SortColumns
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellFolderViewDual3::put_SortColumns


## -description


Sets the names of the columns to be sorted.


## -parameters




### -param bstrSortColumns [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>


          The <b>BSTR</b> that contains the names of the columns to be sorted for the current folder.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



