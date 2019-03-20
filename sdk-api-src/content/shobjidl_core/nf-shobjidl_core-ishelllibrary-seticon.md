---
UID: NF:shobjidl_core.IShellLibrary.SetIcon
title: IShellLibrary::SetIcon (shobjidl_core.h)
author: windows-sdk-content
description: Sets the default icon for the library.
old-location: shell\IShellLibrary_SetIcon.htm
tech.root: shell
ms.assetid: 7d6d6bd5-14cc-432b-b712-64bac78f5df9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IShellLibrary interface [Windows Shell],SetIcon method, IShellLibrary.SetIcon, IShellLibrary::SetIcon, SetIcon, SetIcon method [Windows Shell], SetIcon method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_SetIcon, shell.IShellLibrary_SetIcon, shobjidl_core/IShellLibrary::SetIcon
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IShellLibrary.SetIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellLibrary::SetIcon


## -description


Sets the default icon for the library.


## -parameters




### -param pszIcon [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that describes the location of the default icon. The string must be formatted as <code>ModuleFileName,ResourceIndex</code> or <code>ModuleFileName,-ResourceID</code>. 

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>ModuleFileName</td>
<td>The file name of the module file that contains the icon resource.</td>
</tr>
<tr>
<td>ResourceIndex</td>
<td>A positive decimal number that specifies the index of the icon resource in the module file.</td>
</tr>
<tr>
<td>-ResourceID</td>
<td>A negative decimal number whose absolute value is the resource ID of the icon resource in the module file.</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For more information on the format of the <i>pszIcon</i> parameter, see <a href="https://msdn.microsoft.com/1ded2f0f-0e11-4730-ab7b-16536e7f4435">PathParseIconLocation</a>.




## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/1ded2f0f-0e11-4730-ab7b-16536e7f4435">PathParseIconLocation</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>
 

 

