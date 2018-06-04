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

# IShellFolder2::GetDetailsOf


## -description


Gets detailed information, identified by a column index, on an item in a Shell folder.


## -parameters




### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

PIDL of the item for which you are requesting information. This method accepts only single-level PIDLs. The structure must contain exactly one <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure followed by a terminating zero. If this parameter is set to <b>NULL</b>, the title of the information field specified by <i>iColumn</i> is returned.


### -param iColumn [in]

Type: <b>UINT</b>

The zero-based index of the desired information field. It is identical to the column number of the information as it is displayed in a Windows Explorer Details view.


### -param psd [out]

Type: <b><a href="https://msdn.microsoft.com/2910debb-b769-4498-bd99-9fbf16567e15">SHELLDETAILS</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/2910debb-b769-4498-bd99-9fbf16567e15">SHELLDETAILS</a> structure that contains the information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>IShellFolder2::GetDetailsOf</b> method is identical to <a href="https://msdn.microsoft.com/5442dc80-9ecf-4e47-a84d-6da4327696ef">GetDetailsOf</a>. For a more robust way to retrieve item information that does not require you to know the column index, use <a href="https://msdn.microsoft.com/f006828c-980d-4e36-be68-3b3c238cd884">IShellFolder2::GetDetailsEx</a>.

The <b>IShellFolder2::GetDetailsOf</b> method provides access to the information that is displayed in the Windows Explorer Details view of a Shell folder. The column numbers, headings, and information that you see in the Details view are identical to those of <b>IShellFolder2::GetDetailsOf</b>. Note that the available information fields and their column numbers vary depending on the particular folder. You can enumerate the available fields by calling this method with <i>pidl</i> set to <b>NULL</b>, and examining the title associated with each column index. Bear in mind that these titles can be localized and might not be the same for all locales.

File system folders have a large, standard set of information fields. The first four fields are standard for all file system folders.

<table class="clsStd">
<tr>
<th>Column index</th>
<th>Column title</th>
</tr>
<tr>
<td>0</td>
<td>Name</td>
</tr>
<tr>
<td>1</td>
<td>Size</td>
</tr>
<tr>
<td>2</td>
<td>Type</td>
</tr>
<tr>
<td>3</td>
<td>Date Modified</td>
</tr>
</table>
 

File system folders can support a number of additional fields. However, they are not required to do so, and the column indexes assigned to these fields might vary.

Each virtual folder has its own unique set of information fields. Normally, the item's display name is in column zero, but the order and content of the remaining fields depend on the implementation of the particular folder object.



