---
UID: NF:shlobj.IColumnProvider.GetItemData
title: IColumnProvider::GetItemData
author: windows-sdk-content
description: Requests column data for a specified file.
old-location: shell\IColumnProvider_GetItemData.htm
tech.root: shell
ms.assetid: 88e76f03-acc3-46b1-ad03-d2343f4f3dac
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetItemData, GetItemData method [Windows Shell], GetItemData method [Windows Shell],IColumnProvider interface, IColumnProvider interface [Windows Shell],GetItemData method, IColumnProvider.GetItemData, IColumnProvider::GetItemData, _win32_IColumnProvider_GetItemData, shell.IColumnProvider_GetItemData, shlobj/IColumnProvider::GetItemData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj.h
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
 - IColumnProvider.GetItemData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IColumnProvider::GetItemData


## -description


Requests column data for a specified file.


## -parameters




### -param pscid [in]

Type: <b>LPCSHCOLUMNID</b>

An <a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a> structure that identifies the column.


### -param pscd [in]

Type: <b>LPCSHCOLUMNDATA</b>

An <a href="https://msdn.microsoft.com/3a0c9231-2871-4314-9db3-7e5609e08359">SHCOLUMNDATA</a> structure that specifies the file.


### -param pvarData [out]

Type: <b>VARIANT*</b>

A pointer to a <b>VARIANT</b> with the data for the file specified by <i>pscd</i> that belongs in the column specified by <i>pscid</i>. Set this value if the file is a member of the class supported by the column provider.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if file data is returned, S_FALSE if the file is not supported by the column provider and no data is returned, or a COM error value otherwise.




## -remarks



This method is called to retrieve the data for a file to be displayed in the specified column. It should be thread-safe.

This method is called for every file that Windows Explorer displays, even though many of them will not be supported by a particular column provider. To improve performance, first check the <b>pwszExt</b> member of the structure pointed to by <i>pscd</i> to see if it has a file name extension that is supported by the column provider. If not, avoid unnecessary processing by immediately returning S_FALSE.



