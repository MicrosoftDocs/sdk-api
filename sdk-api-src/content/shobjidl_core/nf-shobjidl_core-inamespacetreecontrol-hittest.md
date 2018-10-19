---
UID: NF:shobjidl_core.INameSpaceTreeControl.HitTest
title: INameSpaceTreeControl::HitTest
author: windows-sdk-content
description: Retrieves the item that a given point is in, if any.
old-location: shell\INameSpaceTreeControl_HitTest.htm
tech.root: shell
ms.assetid: 2287772d-2c06-4d4b-a11e-727dd5de5326
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: HitTest, HitTest method [Windows Shell], HitTest method [Windows Shell],INameSpaceTreeControl interface, INameSpaceTreeControl interface [Windows Shell],HitTest method, INameSpaceTreeControl.HitTest, INameSpaceTreeControl::HitTest, _shell_INameSpaceTreeControl_HitTest, shell.INameSpaceTreeControl_HitTest, shobjidl_core/INameSpaceTreeControl::HitTest
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - INameSpaceTreeControl.HitTest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeControl::HitTest


## -description


Retrieves the item that a given point is in, if any.


## -parameters




### -param ppt [in]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

A pointer to the point to be tested.


### -param ppsiOut [out]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>**</b>

The address of a pointer to the item in which the point exists, or <b>NULL</b> if the point does not exist in an item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function returns <b>S_FALSE</b> with a <b>NULL</b> item if the point does not exist in an item.



