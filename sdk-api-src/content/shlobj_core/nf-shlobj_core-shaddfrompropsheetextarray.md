---
UID: NF:shlobj_core.SHAddFromPropSheetExtArray
title: SHAddFromPropSheetExtArray function
author: windows-sdk-content
description: Adds pages to a property sheet extension array created by SHCreatePropSheetExtArray.
old-location: shell\SHAddFromPropSheetExtArray.htm
tech.root: shell
ms.assetid: e0570cd6-dda2-43e4-8540-58baef37bf18
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: SHAddFromPropSheetExtArray, SHAddFromPropSheetExtArray function [Windows Shell], _win32_SHAddFromPropSheetExtArray, shell.SHAddFromPropSheetExtArray, shlobj_core/SHAddFromPropSheetExtArray
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHAddFromPropSheetExtArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHAddFromPropSheetExtArray function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Adds pages to a property sheet extension array created by <a href="https://msdn.microsoft.com/88a72529-325d-431e-bc26-bddca787e62b">SHCreatePropSheetExtArray</a>.


## -parameters




### -param hpsxa [in]

Type: <b>HPSXA</b>

The array of property sheet handlers returned by <a href="https://msdn.microsoft.com/88a72529-325d-431e-bc26-bddca787e62b">SHCreatePropSheetExtArray</a>.


### -param lpfnAddPage [in]

Type: <b>LPFNADDPROPSHEETPAGE</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb760805(v=VS.85).aspx">AddPropSheetPageProc</a> callback function. It is called once for each property sheet handler. The callback function then returns the information needed to add a page to the handler's property sheet.


### -param lParam

Type: <b>LPARAM</b>

A pointer to application-defined data. This data is passed to the callback function specified by <i>lpfnAddPage</i>.


## -returns



Type: <b>UINT</b>

Returns the number of pages actually added.




## -remarks



This function should be called only once for the property sheet extension array named in <i>hpsxa</i>.

This function calls each extension's <a href="https://msdn.microsoft.com/76a2a94b-b79f-41d1-9e42-fbfda545d12f">IShellPropSheetExt::AddPages</a> method. See that page for further details.




## -see-also




<a href="https://msdn.microsoft.com/88a72529-325d-431e-bc26-bddca787e62b">SHCreatePropSheetExtArray</a>



<a href="https://msdn.microsoft.com/beb3c1b1-deef-440d-8cf7-f76b3f396efa">SHDestroyPropSheetExtArray</a>



<a href="https://msdn.microsoft.com/a8bdde44-d668-46c4-9e58-7a45b775fe09">SHReplaceFromPropSheetExtArray</a>
 

 

