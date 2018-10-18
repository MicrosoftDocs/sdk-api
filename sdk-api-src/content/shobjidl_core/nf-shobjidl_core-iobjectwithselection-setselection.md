---
UID: NF:shobjidl_core.IObjectWithSelection.SetSelection
title: IObjectWithSelection::SetSelection
author: windows-sdk-content
description: Provides the Shell item array that specifies the items included in the selection.
old-location: shell\IObjectWithSelection_SetSelection.htm
tech.root: shell
ms.assetid: e561b8f8-36e9-45ec-beb2-62d7f429dec4
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IObjectWithSelection interface [Windows Shell],SetSelection method, IObjectWithSelection.SetSelection, IObjectWithSelection::SetSelection, SetSelection, SetSelection method [Windows Shell], SetSelection method [Windows Shell],IObjectWithSelection interface, _shell_IObjectWithSelection_SetSelection, shell.IObjectWithSelection_SetSelection, shobjidl_core/IObjectWithSelection::SetSelection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IObjectWithSelection.SetSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectWithSelection::SetSelection


## -description


Provides the Shell item array that specifies the items included in the selection.


## -parameters




### -param psia [in]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a> that represents the selected items.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



