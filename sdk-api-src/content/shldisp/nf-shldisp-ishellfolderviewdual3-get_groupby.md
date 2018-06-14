---
UID: NF:shldisp.IShellFolderViewDual3.get_GroupBy
title: IShellFolderViewDual3::get_GroupBy
author: windows-sdk-content
description: Gets the column used for grouping the folder view.
old-location: shell\IShellFolderViewDual3_get_GroupBy.htm
old-project: shell
ms.assetid: 144fa908-01d3-43f4-95e6-2aad62c23912
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IShellFolderViewDual3 interface [Windows Shell],get_GroupBy method, IShellFolderViewDual3.get_GroupBy, IShellFolderViewDual3::get_GroupBy, _shell_IShellFolderViewDual3_get_GroupBy, get_GroupBy, get_GroupBy method [Windows Shell], get_GroupBy method [Windows Shell],IShellFolderViewDual3 interface, shell.IShellFolderViewDual3_get_GroupBy, shldisp/IShellFolderViewDual3::get_GroupBy
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
 - IShellFolderViewDual3.get_GroupBy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellFolderViewDual3::get_GroupBy


## -description


Gets the column used for grouping the folder view.


## -parameters




### -param pbstrGroupBy [out]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a>*</b>

When this method returns, contains a pointer to the column name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



