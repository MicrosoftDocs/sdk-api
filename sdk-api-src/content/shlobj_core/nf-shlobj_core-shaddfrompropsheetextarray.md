---
UID: NF:shlobj_core.SHAddFromPropSheetExtArray
title: SHAddFromPropSheetExtArray function
author: windows-driver-content
description: Adds pages to a property sheet extension array created by SHCreatePropSheetExtArray.
old-location: shell\SHAddFromPropSheetExtArray.htm
old-project: shell
ms.assetid: e0570cd6-dda2-43e4-8540-58baef37bf18
ms.author: windowsdriverdev
ms.date: 5/7/2018
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
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
api_name:
-	SHAddFromPropSheetExtArray
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
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

A pointer to an <a href="https://msdn.microsoft.com/37673813-89dc-4624-a58b-fe5f44df46c6">AddPropSheetPageProc</a> callback function. It is called once for each property sheet handler. The callback function then returns the information needed to add a page to the handler's property sheet.


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
 

 

