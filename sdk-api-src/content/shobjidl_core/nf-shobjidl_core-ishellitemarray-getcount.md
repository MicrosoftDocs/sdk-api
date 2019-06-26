---
UID: NF:shobjidl_core.IShellItemArray.GetCount
title: IShellItemArray::GetCount (shobjidl_core.h)
author: windows-sdk-content
description: Gets the number of items in the given IShellItem array.
old-location: shell\IShellItemArray_GetCount.htm
tech.root: shell
ms.assetid: 84d20695-bd51-4727-bd82-bd104de99067
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Windows Shell], GetCount method [Windows Shell],IShellItemArray interface, IShellItemArray interface [Windows Shell],GetCount method, IShellItemArray.GetCount, IShellItemArray::GetCount, _shell_IShellItemArray_GetCount, shell.IShellItemArray_GetCount, shobjidl_core/IShellItemArray::GetCount
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IShellItemArray.GetCount"
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
 - IShellItemArray.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellItemArray::GetCount


## -description


Gets the number of items in the given <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> array.


## -parameters




### -param pdwNumItems [out]

Type: <b>DWORD*</b>

When this method returns, contains the number of items in the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getitemat">IShellItemArray::GetItemAt</a>
 

 

