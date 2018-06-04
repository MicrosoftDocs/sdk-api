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

# NPGetPropertyText function


## -description


Retrieves the names of buttons to add to a property dialog box for a network resource.


## -parameters




### -param iButton [in]

Indicates the index of the button. File Manager supports a maximum of six buttons. This parameter is numbered 1-6 for each of the possible buttons if only one file is selected, or 11-16 if multiple files are selected.


### -param nPropSel [in]

Specifies what items the property dialog box focuses on. This can be one of the following values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WNPS_FILE"></a><a id="wnps_file"></a><dl>
<dt><b>WNPS_FILE</b></dt>
</dl>
</td>
<td width="60%">
A single file.

</td>
</tr>
<tr>
<td width="40%"><a id="WNPS_DIR"></a><a id="wnps_dir"></a><dl>
<dt><b>WNPS_DIR</b></dt>
</dl>
</td>
<td width="60%">
A single directory.

</td>
</tr>
<tr>
<td width="40%"><a id="WNPS_MULT"></a><a id="wnps_mult"></a><dl>
<dt><b>WNPS_MULT</b></dt>
</dl>
</td>
<td width="60%">
A selection of multiple files, directories, or both.

</td>
</tr>
</table>
 


### -param lpName [in]

Pointer to a null-terminated string that contains the names of the item or items to be viewed or edited by means of the dialog box. The only supported items are files and directories, so the item names are file names. These should be unambiguous, contain no wildcard characters, and be fully qualified (for example, C:\LOCAL\EXAMPLE.DOC). Multiple file names should be separated with spaces. A file name that contains spaces may be surrounded by quotes (for example, "C:\My File"). In this case. it is treated as a single name. The caret character '^' may also be used as the quotation mechanism for single characters (for example, C:\My^"File, "C:\My^"File" both refer to the file C:\My"File).


### -param lpButtonName [out]

Pointer to a buffer where the network provider should copy the name of the property button. On success, the buffer pointed to by <i>lpButtonName</i> contains the name of the property button. If this buffer, on exit, contains the empty string, then the button corresponding to that name and all succeeding buttons will be removed from the dialog box. The network provider cannot "skip" a button.


### -param nButtonNameLen [in, out]

Specifies the size of the <i>lpButtonName</i> buffer in characters, including the terminating null character.


### -param nType [in]

Specifies the item type, which must be WNTYPE_FILE.


## -returns



If the function succeeds, it should return WN_SUCCESS and <i>lpButtonName</i> can be used. If it points to the empty string, no button corresponds to an index as high as <i>iButton</i>. If the return value is other than WN_SUCCESS, the provider should also call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to set extended error information. Extended error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not load string from resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The given buffer is too small to fit the text of the button.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_VALUE</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpName</i> parameter is an unexpected form.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Property dialog boxes are not supported for the given object type, <i>nType</i>.

</td>
</tr>
</table>
 




## -remarks



File Manager calls this function each time the property dialog box is brought up, and it does this before displaying the dialog box. If the user clicks a button added through this function by the network provider, 
the <a href="https://msdn.microsoft.com/856057f3-2746-4c1e-89a6-6d4e06d0e353">NPPropertyDialog</a> function is called with the appropriate parameters.

Only File Manager calls <b>NPGetPropertyText</b>, and it uses this function for files and directories.



