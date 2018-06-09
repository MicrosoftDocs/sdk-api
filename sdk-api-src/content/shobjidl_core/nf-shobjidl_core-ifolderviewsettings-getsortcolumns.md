---
UID: NF:shobjidl_core.IFolderViewSettings.GetSortColumns
title: IFolderViewSettings::GetSortColumns
author: windows-sdk-content
description: Gets sort column information.
old-location: shell\IFolderViewSettings_GetSortColumns.htm
old-project: shell
ms.assetid: d6115e72-1abc-46fe-b829-0ae1a436b26e
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetSortColumns, GetSortColumns method [Windows Shell], GetSortColumns method [Windows Shell],IFolderViewSettings interface, IFolderViewSettings interface [Windows Shell],GetSortColumns method, IFolderViewSettings.GetSortColumns, IFolderViewSettings::GetSortColumns, _shell_IFolderViewSettings_GetSortColumns, shell.IFolderViewSettings_GetSortColumns, shobjidl_core/IFolderViewSettings::GetSortColumns
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
 - IFolderViewSettings.GetSortColumns
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFolderViewSettings::GetSortColumns


## -description


Gets sort column information.


## -parameters




### -param rgSortColumns [out]

Type: <b><a href="https://msdn.microsoft.com/3ca4c318-6462-4e22-813c-ef7b3ef03230">SORTCOLUMN</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/3ca4c318-6462-4e22-813c-ef7b3ef03230">SORTCOLUMN</a> structures.


### -param cColumnsIn [in]

Type: <b>UINT</b>

The source column count.


### -param pcColumnsOut [out]

Type: <b>UINT*</b>

A pointer to the <i>rgSortColumns</i> array length.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



