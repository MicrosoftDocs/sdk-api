---
UID: NF:shobjidl_core.IShellItemArray.GetItemAt
title: IShellItemArray::GetItemAt
author: windows-sdk-content
description: Gets the item at the given index in the IShellItemArray.
old-location: shell\IShellItemArray_GetItemAt.htm
tech.root: shell
ms.assetid: 58307102-1ae3-4249-81e0-25c1166500d0
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetItemAt, GetItemAt method [Windows Shell], GetItemAt method [Windows Shell],IShellItemArray interface, IShellItemArray interface [Windows Shell],GetItemAt method, IShellItemArray.GetItemAt, IShellItemArray::GetItemAt, _shell_IShellItemArray_GetItemAt, shell.IShellItemArray_GetItemAt, shobjidl_core/IShellItemArray::GetItemAt
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
 - IShellItemArray.GetItemAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellItemArray::GetItemAt


## -description


Gets the item at the given index in the <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>.


## -parameters




### -param dwIndex [in]

Type: <b>DWORD</b>

The index of the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> requested in the <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>



### -param ppsi [out]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>**</b>

When this method returns, contains the requested <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function returns E_FAIL if the requested index is out of bounds of the <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>.




## -see-also




<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>



<a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>



<a href="https://msdn.microsoft.com/84d20695-bd51-4727-bd82-bd104de99067">IShellItemArray::GetCount</a>
 

 

