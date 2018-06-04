---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ShellMessageBoxA function


## -description


<p class="CCE_Message">[<b>ShellMessageBox</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

<b>ShellMessageBox</b> is a special instance of <a href="https://msdn.microsoft.com/4840decc-8173-4021-8d3e-bae3b0eaa956">MessageBox</a> that provides the option of using the owner window's title as the title of the message box.
  


## -parameters




### -param hAppInst

TBD


### -param hWnd [in]

Type: <b>HWND</b>

A handle to the owner window of the message box to be created. If this variable is not <b>NULL</b>, the title of the owner window is used as the title of the message box.


### -param lpcText

TBD


### -param lpcTitle

TBD


### -param fuStyle [in]

Type: <b>UINT</b>

Specifies the contents and behavior of the dialog box. For possible values, see <a href="https://msdn.microsoft.com/4840decc-8173-4021-8d3e-bae3b0eaa956">MessageBox</a>.


### -param param

TBD




####### - ... [in]

A variable argument list that is combined with <i>pszMsg</i> to form the full text displayed in the message box.


#### - hInst [in]

Type: <b>HINSTANCE</b>

The handle of the module from which to load a string resource named in <i>pszTitle</i>. If <i>pszTitle</i> does not name a string resource, this parameter is ignored. This value must be valid if <i>pszMsg</i> or <i>pszTitle</i> is a resource ID.


#### - pszMsg [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains either the message to be displayed or a resource ID specifying where the message is to be retrieved from.


#### - pszTitle [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the dialog box title or a resource ID specifying where the title is to be retrieved. If both this parameter and <i>hWnd</i> are <b>NULL</b>, no title is displayed. If this parameter points to a loadable resource formed with the <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a> macro, it overrides <i>hWnd</i> as the title.


## -returns



Type: <b>int</b>

An integer value indicating a button that was pressed in the message box. For specific values, see <a href="https://msdn.microsoft.com/4840decc-8173-4021-8d3e-bae3b0eaa956">MessageBox</a>.

					

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>



<a href="https://msdn.microsoft.com/4840decc-8173-4021-8d3e-bae3b0eaa956">MessageBox</a>
 

 

