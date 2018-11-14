---
UID: NF:shobjidl_core.IShellItemArray.EnumItems
title: IShellItemArray::EnumItems
author: windows-sdk-content
description: Gets an enumerator of the items in the array.
old-location: shell\IShellItemArray_EnumItems.htm
tech.root: shell
ms.assetid: c8ee210c-dab9-4678-9c62-d06677cbb395
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: EnumItems, EnumItems method [Windows Shell], EnumItems method [Windows Shell],IShellItemArray interface, IShellItemArray interface [Windows Shell],EnumItems method, IShellItemArray.EnumItems, IShellItemArray::EnumItems, _shell_IShellItemArray_EnumItems, shell.IShellItemArray_EnumItems, shobjidl_core/IShellItemArray::EnumItems
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
 - IShellItemArray.EnumItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- IShellItemArray.EnumItems
: 
---

# IShellItemArray::EnumItems


## -description


Gets an enumerator of the items in the array.


## -parameters




### -param ppenumShellItems [out]

Type: <b><a href="https://msdn.microsoft.com/07aed597-359f-4f4b-9edf-168c15bdc58e">IEnumShellItems</a>**</b>

When this method returns, contains an <a href="https://msdn.microsoft.com/07aed597-359f-4f4b-9edf-168c15bdc58e">IEnumShellItems</a> pointer that enumerates the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">shell items</a> that are in the array.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>



<a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>
 

 

