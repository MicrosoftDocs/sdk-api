---
UID: NF:exdisp.IShellWindows._NewEnum
title: IShellWindows::_NewEnum
author: windows-sdk-content
description: Retrieves an enumerator for the collection of Shell windows.
old-location: shell\IShellWindows_NewEnum.htm
tech.root: shell
ms.assetid: e91b2be7-2be9-4460-9a2a-57090dcfc961
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IShellWindows interface [Windows Shell],_NewEnum method, IShellWindows._NewEnum, IShellWindows::_NewEnum, _NewEnum, _NewEnum method [Windows Shell], _NewEnum method [Windows Shell],IShellWindows interface, _win32_IShellWindows_NewEnum, exdisp/IShellWindows::_NewEnum, shell.IShellWindows_NewEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: exdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Exdisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shdocvw.dll (version 5.00.2014.0216 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IShellWindows._NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5
---

# IShellWindows::_NewEnum


## -description


Retrieves an enumerator for the collection of Shell windows.


## -parameters




### -param ppunk [out, retval]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

When this method returns, contains an interface pointer to an object that implements the <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e609c8b6-2b2e-4188-894c-5c85960206ea">IShellWindows</a>



<a href="https://msdn.microsoft.com/04157d1a-8a4d-4ffd-882d-41748408ba2b">IShellWindows::Item</a>



<a href="https://msdn.microsoft.com/50781569-4c80-4304-96f3-8a135cea3b20">IShellWindows::get_Count</a>
 

 

