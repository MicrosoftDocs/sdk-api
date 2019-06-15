---
UID: NF:winuser.GetListBoxInfo
title: GetListBoxInfo function (winuser.h)
author: windows-sdk-content
description: Retrieves the number of items per column in a specified list box.
old-location: controls\GetListBoxInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxfunctions\getlistboxinfo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetListBoxInfo, GetListBoxInfo function [Windows Controls], _win32_GetListBoxInfo, _win32_GetListBoxInfo_cpp, controls.GetListBoxInfo, controls._win32_GetListBoxInfo, winuser/GetListBoxInfo
ms.topic: function
f1_keywords: ["winuser/GetListBoxInfo"]
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetListBoxInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: Service Pack 6
ms.custom: 19H1
---

# GetListBoxInfo function


## -description


Retrieves the number of items per column in a specified list box. 


## -parameters




### -param hwnd [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list box whose number of items per column is to be retrieved. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The return value is the number of items per column.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getcomboboxinfo">GetComboBoxInfo</a>
 

 

