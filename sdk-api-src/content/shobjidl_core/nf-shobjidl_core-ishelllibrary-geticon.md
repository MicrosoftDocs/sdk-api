---
UID: NF:shobjidl_core.IShellLibrary.GetIcon
title: IShellLibrary::GetIcon
author: windows-sdk-content
description: Gets the default icon for the library.
old-location: shell\IShellLibrary_GetIcon.htm
tech.root: shell
ms.assetid: e39bd663-3f2d-4b72-9882-1313ee457844
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetIcon, GetIcon method [Windows Shell], GetIcon method [Windows Shell],IShellLibrary interface, IShellLibrary interface [Windows Shell],GetIcon method, IShellLibrary.GetIcon, IShellLibrary::GetIcon, _shell_IShellLibrary_GetIcon, shell.IShellLibrary_GetIcon, shobjidl_core/IShellLibrary::GetIcon
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IShellLibrary.GetIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellLibrary::GetIcon


## -description


Gets the default icon for the library.


## -parameters




### -param ppszIcon [out]

Type: <b>LPWSTR*</b>

A null-terminated Unicode string that describes the location of the default icon. The  string is returned as <code>ModuleFileName,ResourceIndex</code> or <code>ModuleFileName,-ResourceID</code>. 

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
<td>If the number that follows the comma is positive, the index of the resource in the module file.</td>
</tr>
<tr>
<td>-ResourceID</td>
<td>If the number that follows the comma is negative, the absolute value of the number is the resource ID of the icon in the module file.</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For additional information on parsing the string returned in <i>ppszIcon</i>, see <a href="https://msdn.microsoft.com/1ded2f0f-0e11-4730-ab7b-16536e7f4435">PathParseIconLocation</a>.




## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/12F6E6AE-2776-408c-B9AC-E885BE93C27F">Library Description Schema</a>



<a href="https://msdn.microsoft.com/1ded2f0f-0e11-4730-ab7b-16536e7f4435">PathParseIconLocation</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>
 

 

