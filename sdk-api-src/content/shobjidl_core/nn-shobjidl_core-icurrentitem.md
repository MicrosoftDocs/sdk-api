---
UID: NN:shobjidl_core.ICurrentItem
title: ICurrentItem
author: windows-sdk-content
description: Obtained by calling IShellFolder::BindToObject for an item. If the item represents a snapshot of an item at a previous time, this interface will obtain the current version of the item.
old-location: shell\ICurrentItem.htm
tech.root: shell
ms.assetid: a5ff7199-134d-4c1a-91e0-a81ff474f5a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICurrentItem, ICurrentItem interface [Windows Shell], ICurrentItem interface [Windows Shell],described, _shell_ICurrentItem, shell.ICurrentItem, shobjidl_core/ICurrentItem
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: 
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
 - ICurrentItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICurrentItem interface


## -description


Obtained by calling <a href="https://msdn.microsoft.com/5e699494-1974-4b9b-8324-9394f7b96fe4">IShellFolder::BindToObject</a> for an item. If the item represents a snapshot of an item at a previous time, this interface will obtain the current version of the item.


## -remarks



This interface provides only the methods of the <a href="https://msdn.microsoft.com/f42d218c-0251-45e0-b05a-f1ccdcaf036c">IRelatedItem</a> interface, from which it inherits.



