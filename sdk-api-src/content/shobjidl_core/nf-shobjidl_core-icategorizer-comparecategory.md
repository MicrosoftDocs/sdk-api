---
UID: NF:shobjidl_core.ICategorizer.CompareCategory
title: ICategorizer::CompareCategory
author: windows-sdk-content
description: Determines the relative order of two items in their item identifier lists, and hence in the UI.
old-location: shell\ICategorizer_CompareCategory.htm
old-project: shell
ms.assetid: 25775fa5-595d-4911-9cd4-47fde429b923
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CompareCategory, CompareCategory method [Windows Shell], CompareCategory method [Windows Shell],ICategorizer interface, ICategorizer interface [Windows Shell],CompareCategory method, ICategorizer.CompareCategory, ICategorizer::CompareCategory, inet_ICategorizer_CompareCategory, shell.ICategorizer_CompareCategory, shobjidl_core/ICategorizer::CompareCategory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICategorizer.CompareCategory
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# ICategorizer::CompareCategory


## -description


Determines the relative order of two items in their item identifier lists, and hence in the UI.


## -parameters




### -param csfFlags

Type: <b><a href="https://msdn.microsoft.com/5e3f6c84-ebc4-45e7-8272-f5d98bffd4c8">CATSORT_FLAGS</a></b>

A flag that specifies how the comparison should be performed. The parameter should be one of the values in <a href="https://msdn.microsoft.com/5e3f6c84-ebc4-45e7-8272-f5d98bffd4c8">CATSORT_FLAGS</a>.


### -param dwCategoryId1

Type: <b>DWORD</b>

A <b>DWORD</b> that specifies the first category identifier to use in the comparison.


### -param dwCategoryId2

Type: <b>DWORD</b>

A <b>DWORD</b> that specifies the second category identifier to use in the comparison.


## -returns



Type: <b>HRESULT</b>

If this method is successful, the CODE field of the HRESULT contains a value that specifies the outcome of the comparison, otherwise it returns a COM error code.




## -remarks



The following table shows the values returned in the CODE field of the HRESULT.

    			


<table class="clsStd">
<tr>
<td>Less than zero </td>
<td>The first item should precede the second (<i>dwCategoryId1</i> &lt; <i>dwCategoryId2</i>).</td>
</tr>
<tr>
<td>Greater than zero </td>
<td>The first item should follow the second (<i>dwCategoryId1</i> &gt; <i>dwCategoryId2</i>).</td>
</tr>
<tr>
<td>Zero </td>
<td>The two items are the same (<i>dwCategoryId1</i> = <i>dwCategoryId2</i>).</td>
</tr>
</table>
 





