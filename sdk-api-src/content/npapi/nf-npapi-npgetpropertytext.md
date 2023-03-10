---
UID: NF:npapi.NPGetPropertyText
title: NPGetPropertyText function (npapi.h)
description: Retrieves the names of buttons to add to a property dialog box for a network resource.
helpviewer_keywords: ["NPGetPropertyText","NPGetPropertyText function [Security]","WNPS_DIR","WNPS_FILE","WNPS_MULT","_mnp_npgetpropertytext","npapi/NPGetPropertyText","security.npgetpropertytext"]
old-location: security\npgetpropertytext.htm
tech.root: security
ms.assetid: 5c4583f5-81e9-4723-8fd0-6909b0107446
ms.date: 12/05/2018
ms.keywords: NPGetPropertyText, NPGetPropertyText function [Security], WNPS_DIR, WNPS_FILE, WNPS_MULT, _mnp_npgetpropertytext, npapi/NPGetPropertyText, security.npgetpropertytext
req.header: npapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NPGetPropertyText
 - npapi/NPGetPropertyText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - NPGetPropertyText
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

If the function succeeds, it should return WN_SUCCESS and <i>lpButtonName</i> can be used. If it points to the empty string, no button corresponds to an index as high as <i>iButton</i>. If the return value is other than WN_SUCCESS, the provider should also call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> to set extended error information. Extended error codes include the following.

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
the <a href="/windows/desktop/api/npapi/nf-npapi-nppropertydialog">NPPropertyDialog</a> function is called with the appropriate parameters.

Only File Manager calls <b>NPGetPropertyText</b>, and it uses this function for files and directories.