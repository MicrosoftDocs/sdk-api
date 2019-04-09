---
UID: NF:shlobj_core.IActiveDesktop.AddUrl
title: IActiveDesktop::AddUrl (shlobj_core.h)
author: windows-sdk-content
description: Adds the desktop item associated with the specified URL.
old-location: lwef\iactivedesktop_addurl_method.htm
tech.root: lwef
ms.assetid: 295b2f46-6178-4aef-9721-8105c75a4a55
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddUrl, AddUrl method [Legacy Windows Environment Features], AddUrl method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],AddUrl method, IActiveDesktop.AddUrl, IActiveDesktop::AddUrl, _win32_IActiveDesktop_AddUrl_Method, lwef.iactivedesktop_addurl_method, shell.iactivedesktop_addurl_method, shlobj_core/IActiveDesktop::AddUrl
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IActiveDesktop.AddUrl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveDesktop::AddUrl


## -description


Adds the desktop item associated with the specified URL.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window for the user interface. 


### -param pszSource [in]

Type: <b>PCWSTR</b>

A pointer to a string that contains the URL of the desktop item. 


### -param pcomp [in]

Type: <b>LPCOMPONENT</b>

A pointer to the <a href="https://msdn.microsoft.com/2692a2d6-1d33-410f-987c-8388c636cae6">COMPONENT</a> structure that contains the details of the desktop item to be added. 


### -param dwFlags

Type: <b>DWORD</b>

An unsigned long integer value that controls this method. Can be set to ADDURL_SILENT to add a desktop item without displaying any user interfaces.


## -returns



Type: <b>HRESULT</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failed to add the desktop item or an instance of the desktop item already exists on the Active Desktop.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVAILDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
If the ADDURL_SILENT flag has been set, the desktop item has either been added successfully or it already exists on the Active Desktop. Otherwise, the desktop item has been added succesfully.

</td>
</tr>
</table>
 




## -remarks



By default, this method will display some user interface and then add the desktop item to the Active Desktop. Like <a href="https://msdn.microsoft.com/5a0c61e8-a645-4a32-b97b-8d7b43d0e5e3">IActiveDesktop::AddDesktopItem</a>, the client application must call <a href="https://msdn.microsoft.com/3bac5af5-f4a6-4822-83de-11633beef88a">IActiveDesktop::ApplyChanges</a> to have the changes saved to the registry.




## -see-also




<a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>



<a href="https://msdn.microsoft.com/68d72b0f-f5e9-4fff-bb13-4c60d1dd7009">Using the Active Desktop Object</a>
 

 

