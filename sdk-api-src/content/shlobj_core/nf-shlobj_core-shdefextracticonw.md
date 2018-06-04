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

# SHDefExtractIconW function


## -description


Provides a default handler to extract an icon from a file.


## -parameters




### -param pszIconFile [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated buffer that contains the path and name of the file from which the icon is extracted.


### -param iIndex

Type: <b>int</b>

The location of the icon within the file named in <i>pszIconFile</i>. If this is a positive number, it refers to the zero-based position of the icon in the file. For instance, 0 refers to the 1st icon in the resource file and 2 refers to the 3rd. If this is a negative number, it refers to the icon's resource ID.


### -param uFlags [in]

Type: <b>UINT</b>

A flag that controls the icon extraction.



#### GIL_SIMULATEDOC

Overlays the extracted icon on the default document icon to create the final icon. This icon can be used when no more appropriate icon can be found or retrieved.


### -param phiconLarge [out, optional]

Type: <b>HICON*</b>

A pointer to an HICON that, when this function returns successfully, receives the handle of the large version of the icon specified in the <a href="https://msdn.microsoft.com/4f169f33-ed13-4efc-bf3f-ea2a4fe1de4e">LOWORD</a> of <i>nIconSize</i>. This value can be <b>NULL</b>.


### -param phiconSmall [out, optional]

Type: <b>HICON*</b>

A pointer to an HICON that, when this function returns successfully, receives the handle of the small version of the icon specified in the <a href="https://msdn.microsoft.com/9f79d489-ff3f-437c-821e-fd353d712c7b">HIWORD</a> of <i>nIconSize</i>.


### -param nIconSize

Type: <b>UINT</b>

A value that contains the large icon size in its <a href="https://msdn.microsoft.com/4f169f33-ed13-4efc-bf3f-ea2a4fe1de4e">LOWORD</a> and the small icon size in its <a href="https://msdn.microsoft.com/9f79d489-ff3f-437c-821e-fd353d712c7b">HIWORD</a>. Size is measured in pixels. Pass 0 to specify default large and small sizes.


##### - uFlags.GIL_SIMULATEDOC

Overlays the extracted icon on the default document icon to create the final icon. This icon can be used when no more appropriate icon can be found or retrieved.


## -returns



Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The requested icon is not present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The file cannot be accessed, or is being accessed through a slow link.

</td>
</tr>
</table>
 




## -remarks



It is the responsibility of the caller to free the icon resources created through this function when they are no longer needed. This can be done through the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function.



