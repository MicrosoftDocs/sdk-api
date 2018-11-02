---
UID: NF:shlobj_core.IShellDetails.ColumnClick
title: IShellDetails::ColumnClick
author: windows-sdk-content
description: Rearranges a column.
old-location: shell\IShellDetails_ColumnClick.htm
tech.root: shell
ms.assetid: df37b2c7-16ea-4768-a1c2-6ccec4fecde9
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ColumnClick, ColumnClick method [Windows Shell], ColumnClick method [Windows Shell],IShellDetails interface, IShellDetails interface [Windows Shell],ColumnClick method, IShellDetails.ColumnClick, IShellDetails::ColumnClick, _win32_IShellDetails_ColumnClick, shell.IShellDetails_ColumnClick, shlobj_core/IShellDetails::ColumnClick
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellDetails.ColumnClick
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellDetails::ColumnClick


## -description


Rearranges a column.


## -parameters




### -param iColumn

Type: <b>UINT</b>

The index of the column to be rearranged.


## -returns



Type: <b>HRESULT</b>

Returns S_FALSE to tell the calling application to sort the selected column. Otherwise, returns S_OK if successful, a COM error code otherwise.




## -remarks



This method is called when a client of a folder object wants to sort the object's items based on the contents of one of the Details columns. Folder objects typically return S_FALSE.

<h3><a id="Note_to_Implementers"></a><a id="note_to_implementers"></a><a id="NOTE_TO_IMPLEMENTERS"></a>Note to Implementers</h3>
For Windows 2000 and later systems, folder objects should implement <a href="https://msdn.microsoft.com/9b008034-3576-429e-b67c-e2222592ca46">IShellFolder2</a> instead of this interface. However, if your application needs to function on earlier systems, it should also expose <a href="https://msdn.microsoft.com/c31409fd-9350-46bb-a8a0-85d5958c6e49">IShellDetails</a>.




## -see-also




<a href="https://msdn.microsoft.com/c31409fd-9350-46bb-a8a0-85d5958c6e49">IShellDetails</a>



<a href="https://msdn.microsoft.com/5442dc80-9ecf-4e47-a84d-6da4327696ef">IShellDetails::GetDetailsOf</a>
 

 

