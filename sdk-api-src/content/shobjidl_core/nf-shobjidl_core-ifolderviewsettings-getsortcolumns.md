---
UID: NF:shobjidl_core.IFolderViewSettings.GetSortColumns
title: IFolderViewSettings::GetSortColumns (shobjidl_core.h)
description: Gets sort column information.
helpviewer_keywords: ["GetSortColumns","GetSortColumns method [Windows Shell]","GetSortColumns method [Windows Shell]","IFolderViewSettings interface","IFolderViewSettings interface [Windows Shell]","GetSortColumns method","IFolderViewSettings.GetSortColumns","IFolderViewSettings::GetSortColumns","_shell_IFolderViewSettings_GetSortColumns","shell.IFolderViewSettings_GetSortColumns","shobjidl_core/IFolderViewSettings::GetSortColumns"]
old-location: shell\IFolderViewSettings_GetSortColumns.htm
tech.root: shell
ms.assetid: d6115e72-1abc-46fe-b829-0ae1a436b26e
ms.date: 12/05/2018
ms.keywords: GetSortColumns, GetSortColumns method [Windows Shell], GetSortColumns method [Windows Shell],IFolderViewSettings interface, IFolderViewSettings interface [Windows Shell],GetSortColumns method, IFolderViewSettings.GetSortColumns, IFolderViewSettings::GetSortColumns, _shell_IFolderViewSettings_GetSortColumns, shell.IFolderViewSettings_GetSortColumns, shobjidl_core/IFolderViewSettings::GetSortColumns
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFolderViewSettings::GetSortColumns
 - shobjidl_core/IFolderViewSettings::GetSortColumns
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
 - IFolderViewSettings.GetSortColumns
---

# IFolderViewSettings::GetSortColumns


## -description

Gets sort column information.

## -parameters

### -param rgSortColumns [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-sortcolumn">SORTCOLUMN</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-sortcolumn">SORTCOLUMN</a> structures.

### -param cColumnsIn [in]

Type: <b>UINT</b>

The source column count.

### -param pcColumnsOut [out]

Type: <b>UINT*</b>

A pointer to the <i>rgSortColumns</i> array length.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.