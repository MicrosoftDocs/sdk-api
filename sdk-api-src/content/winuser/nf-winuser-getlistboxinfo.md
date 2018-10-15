---
UID: NF:winuser.GetListBoxInfo
title: GetListBoxInfo function
author: windows-sdk-content
description: Retrieves the number of items per column in a specified list box.
old-location: controls\GetListBoxInfo.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxfunctions\getlistboxinfo.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetListBoxInfo, GetListBoxInfo function [Windows Controls], _win32_GetListBoxInfo, _win32_GetListBoxInfo_cpp, controls.GetListBoxInfo, controls._win32_GetListBoxInfo, winuser/GetListBoxInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
---

# GetListBoxInfo function


## -description


Retrieves the number of items per column in a specified list box. 


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list box whose number of items per column is to be retrieved. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The return value is the number of items per column.




## -see-also




<a href="https://msdn.microsoft.com/f7553df7-4309-49fc-9e4a-da9063e6b042">GetComboBoxInfo</a>
 

 

