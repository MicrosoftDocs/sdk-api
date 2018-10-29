---
UID: NF:shobjidl_core.IObjectWithSelection.GetSelection
title: IObjectWithSelection::GetSelection
author: windows-sdk-content
description: Gets the Shell item array that contains the selected items.
old-location: shell\IObjectWithSelection_GetSelection.htm
tech.root: shell
ms.assetid: cc0c2c79-a475-4384-8255-809dc8bdb869
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetSelection, GetSelection method [Windows Shell], GetSelection method [Windows Shell],IObjectWithSelection interface, IObjectWithSelection interface [Windows Shell],GetSelection method, IObjectWithSelection.GetSelection, IObjectWithSelection::GetSelection, _shell_IObjectWithSelection_GetSelection, shell.IObjectWithSelection_GetSelection, shobjidl_core/IObjectWithSelection::GetSelection
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
 - IObjectWithSelection.GetSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectWithSelection::GetSelection


## -description


Gets the Shell item array that contains the selected items.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IShellItemArray.


### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically an <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



We recommend that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.



