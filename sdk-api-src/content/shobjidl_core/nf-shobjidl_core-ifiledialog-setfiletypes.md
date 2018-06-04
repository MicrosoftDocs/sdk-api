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

# IFileDialog::SetFileTypes


## -description


Sets the file types that the dialog can open or save.


## -parameters




### -param cFileTypes [in]

Type: <b>UINT</b>

The number of elements in the array specified by <i>rgFilterSpec</i>.


### -param rgFilterSpec [in]

Type: <b>const <a href="https://msdn.microsoft.com/b5bb6777-a5b6-4d10-a8b8-79269fa5e2da">COMDLG_FILTERSPEC</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/b5bb6777-a5b6-4d10-a8b8-79269fa5e2da">COMDLG_FILTERSPEC</a> structures, each representing a file type.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/ca850988-7f2f-4faf-9ded-14db476fc452">SetFileTypes</a> has already been called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <b>FOS_PICKFOLDERS</b> flag was set in the <a href="https://msdn.microsoft.com/99def5c2-3fc3-416c-80a6-6009927ab63e">IFileDialog::SetOptions</a> method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>rgFilterSpec</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



When using the <b>Open</b> dialog, the file types declared there are used to filter the view. When using the <b>Save</b> dialog, these values determine which file name extension is appended to the file name.

This method must be called before the dialog is shown and can only be called once for each dialog instance. File types cannot be modified once the Common Item dialog box is displayed.


#### Examples

The following code example demonstrates the use of the array of <a href="https://msdn.microsoft.com/b5bb6777-a5b6-4d10-a8b8-79269fa5e2da">COMDLG_FILTERSPEC</a> structures in the context of this method. The example array consists of three <b>COMDLG_FILTERSPEC</b> structures. The first declares two patterns for the dialog filter, the second declares a single pattern, and the last shows files of all types. The variables szJPG, szBMP, and szAll are assumed to be previously declared strings that provide a friendly name for each filter.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>COMDLG_FILTERSPEC rgSpec[] =
{ 
    { szJPG, L"*.jpg;*.jpeg" },
    { szBMP, L"*.bmp" },
    { szAll, L"*.*" },
};</pre>
</td>
</tr>
</table></span></div>


