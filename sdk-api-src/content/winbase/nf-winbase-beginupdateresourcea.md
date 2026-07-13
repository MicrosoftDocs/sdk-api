---
UID: NF:winbase.BeginUpdateResourceA
title: BeginUpdateResourceA function (winbase.h)
description: Retrieves a handle that can be used by the UpdateResource function to add, delete, or replace resources in a binary module. (ANSI)
helpviewer_keywords: ["BeginUpdateResourceA", "winbase/BeginUpdateResourceA"]
old-location: menurc\beginupdateresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\beginupdateresource.htm
ms.date: 12/05/2018
ms.keywords: BeginUpdateResource, BeginUpdateResource function [Menus and Other Resources], BeginUpdateResourceA, BeginUpdateResourceW, _win32_BeginUpdateResource, _win32_beginupdateresource_cpp, menurc.beginupdateresource, winbase/BeginUpdateResource, winbase/BeginUpdateResourceA, winbase/BeginUpdateResourceW, winui._win32_beginupdateresource
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: BeginUpdateResourceW (Unicode) and BeginUpdateResourceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BeginUpdateResourceA
 - winbase/BeginUpdateResourceA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-kernel32-updateresource-l1-1-0.dll
 - Kernel32.dll
api_name:
 - BeginUpdateResource
 - BeginUpdateResourceA
 - BeginUpdateResourceW
---

# BeginUpdateResourceA function


## -description

Retrieves a handle that can be used by the <a href="/windows/desktop/api/winbase/nf-winbase-updateresourcea">UpdateResource</a> function to add, delete, or replace resources in a binary module.

## -parameters

### -param pFileName [in]

Type: <b>LPCTSTR</b>

The binary file in which to update resources. An application must be able to obtain write-access to this file; the file referenced by <i>pFileName</i> cannot be currently executing. If <i>pFileName</i> does not specify a full path, the system searches for the file in the current directory.

### -param bDeleteExistingResources [in]

Type: <b>BOOL</b>

Indicates whether to delete the <i>pFileName</i> parameter's existing resources. If this parameter is <b>TRUE</b>, existing resources are deleted and the updated file includes only resources added with the <a href="/windows/desktop/api/winbase/nf-winbase-updateresourcea">UpdateResource</a> function. If this parameter is <b>FALSE</b>, the updated file includes existing resources unless they are explicitly deleted or replaced by using <b>UpdateResource</b>.

## -returns

Type: <b>HANDLE</b>

If the function succeeds, the return value is a handle that can be used by the <a href="/windows/desktop/api/winbase/nf-winbase-updateresourcea">UpdateResource</a> and <a href="/windows/desktop/api/winbase/nf-winbase-endupdateresourcea">EndUpdateResource</a> functions. The return value is <b>NULL</b> if the specified file is not a PE, the file does not exist, or the file cannot be opened for writing. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

It is recommended that the resource file is not loaded before this function is called. However, if that file is already loaded, it will not cause an error to be returned.

There are some restrictions on resource updates in files that contain  Resource Configuration(RC Config) data: LN files and the associated .mui files. Details on which types of resources are allowed to be updated in these files are in the Remarks section for the <a href="/windows/desktop/api/winbase/nf-winbase-updateresourcea">UpdateResource</a> function.

This function can update resources within modules that contain both code and resources. As noted above, there are restrictions on resource updates in LN files and .mui files, both of which contain RC Config data; details of the restrictions are in the reference for the <a href="/windows/desktop/api/winbase/nf-winbase-updateresourcea">UpdateResource</a> function.
			


#### Examples

For an example see, <a href="/windows/desktop/menurc/using-resources">Updating Resources</a>.

<div class="code"></div>




> [!NOTE]
> The winbase.h header defines BeginUpdateResource as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winbase/nf-winbase-endupdateresourcea">EndUpdateResource</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/resources">Resources</a>



<a href="/windows/desktop/api/winbase/nf-winbase-updateresourcea">UpdateResource</a>
