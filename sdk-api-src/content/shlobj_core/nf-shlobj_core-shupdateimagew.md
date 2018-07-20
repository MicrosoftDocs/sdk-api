---
UID: NF:shlobj_core.SHUpdateImageW
title: SHUpdateImageW function
author: windows-sdk-content
description: Notifies the Shell that an image in the system image list has changed.
old-location: shell\SHUpdateImage.htm
old-project: shell
ms.assetid: 9df5860e-db65-4e43-aaf9-c1e0e33fc569
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: SHUpdateImage, SHUpdateImage function [Windows Shell], SHUpdateImageA, SHUpdateImageW, _win32_SHUpdateImage, shell.SHUpdateImage, shlobj_core/SHUpdateImage, shlobj_core/SHUpdateImageA, shlobj_core/SHUpdateImageW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHUpdateImageW (Unicode) and SHUpdateImageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHUpdateImage
 - SHUpdateImageA
 - SHUpdateImageW
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.7 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHUpdateImageW function


## -description


Notifies the Shell that an image in the system image list has changed.


## -parameters




### -param pszHashItem [in]

Type: <b>LPCTSTR</b>

A pointer to a string value that specifies the fully qualified path of the file that contains the icon. Use the path that is returned in the buffer pointed to by the <i>szIconFile</i> parameter of <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a>.


### -param iIndex [in]

Type: <b>int</b>

An integer that specifies the zero-based index of the icon in the file specified by <i>pszHashItem</i>. Use the value that is pointed to by the <i>piIndex</i> parameter of <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a>.


### -param uFlags [in]

Type: <b>UINT</b>

An unsigned integer that specifies the flags that determine the icon attributes. Set <i>uFlags</i> to the value that is pointed to by the <i>pwFlags</i> parameter of <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a>. The flags that are relevant to <b>SHUpdateImage</b> are <b>GIL_NOTFILENAME</b> and <b>GIL_SIMULATEDOC</b>.


### -param iImageIndex [in]

Type: <b>int</b>

An integer that specifies the index in the system image list of the icon that is being updated.


## -returns



No return value.




## -remarks



If you do not know the index in the system image list of the icon that you want to update, use <a href="https://msdn.microsoft.com/d662bedf-4be0-4528-8121-e7923a42bc67">SHGetFileInfo</a> with the <i>uFlags</i> parameter set to <b>SHGFI_SYSICONINDEX</b>.

You must use <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a> with the parameters of the old icon that needs to be updated, not those of the new icon you want to replace it with.




## -see-also




<a href="https://msdn.microsoft.com/a9222ce9-0d06-4fd0-af3a-fd0e979713ce">SHChangeNotify</a>
 

 

