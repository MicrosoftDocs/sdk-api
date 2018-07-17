---
UID: NF:shldisp.IShellDispatch3.AddToRecent
title: IShellDispatch3::AddToRecent
author: windows-sdk-content
description: Adds a file to the most recently used (MRU) list.
old-location: shell\IShellDispatch3_AddToRecent.htm
old-project: shell
ms.assetid: aa5aef31-7f3f-4cc4-949d-1484de243ef3
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: AddToRecent, AddToRecent method [Windows Shell], AddToRecent method [Windows Shell],IShellDispatch3 object, IShellDispatch3 object [Windows Shell],AddToRecent method, IShellDispatch3.AddToRecent, IShellDispatch3::AddToRecent, _shell_IShellDispatch3_AddToRecent, shell.IShellDispatch3_AddToRecent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellDispatch3.AddToRecent
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch3::AddToRecent


## -description


Adds a file to the most recently used (MRU) list.


## -parameters




### -param varFile [in]

Type: <b>Variant</b>

A <b>String</b> that contains the path of the file to add to the list of recently used documents.
                        
                        

<b>Windows Vista</b>: Set this parameter to <b>null</b> to clear the recent documents folder.


### -param bstrCategory [in, optional]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

A <b>String</b> that contains the name of the category in which to place the file.


## -returns



<h3>JScript</h3>
This method does not return a value.

<h3>VB</h3>
This method does not return a value.



