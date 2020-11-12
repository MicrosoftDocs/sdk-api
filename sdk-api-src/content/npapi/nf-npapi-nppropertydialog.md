---
UID: NF:npapi.NPPropertyDialog
title: NPPropertyDialog function (npapi.h)
description: Called when the user clicks a button added by using the NPPropertyDialog function. The NPPropertyDialog function is called only for file and directory network properties.
helpviewer_keywords: ["NPPropertyDialog","NPPropertyDialog function [Security]","WNPS_DIR","WNPS_FILE","WNPS_MULT","_mnp_nppropertydialog","npapi/NPPropertyDialog","security.nppropertydialog"]
old-location: security\nppropertydialog.htm
tech.root: security
ms.assetid: 856057f3-2746-4c1e-89a6-6d4e06d0e353
ms.date: 12/05/2018
ms.keywords: NPPropertyDialog, NPPropertyDialog function [Security], WNPS_DIR, WNPS_FILE, WNPS_MULT, _mnp_nppropertydialog, npapi/NPPropertyDialog, security.nppropertydialog
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
 - NPPropertyDialog
 - npapi/NPPropertyDialog
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
 - NPPropertyDialog
---

# NPPropertyDialog function


## -description

Called when the user clicks a button added by using the <b>NPPropertyDialog</b> function. The <b>NPPropertyDialog</b> function is called only for file and directory network properties.

## -parameters

### -param hwndParent [in]

A handle to the parent window that should own the file property dialog box.

### -param iButtonDlg [in]

The index of the button that was pressed. 




This index specifies which property dialog box was requested, starting with one for the first button returned from 
the <a href="/windows/desktop/api/npapi/nf-npapi-npgetpropertytext">NPGetPropertyText</a> function. If there are multiple file names selected, 10 is added to this number. In other words, if there is more than one file selected and the user presses the first provider-defined property button, <i>iButtonDlg</i> will be 11. If there is only one file selected and the user presses the second network property button, <i>iButtonDlg</i> will be two.

### -param nPropSel [in]

Specifies what items the property dialog box should act on. This parameter can be one of the following values. 




					

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

### -param lpFileName [in]

A pointer to the names of the items that the property dialog box should act on. The only supported items are files and directories, so the item names are file names. These should be unambiguous, contain no wildcard characters, and  be fully qualified, for example, <b>C:\Local\\</b><i>Example</i><b>.doc</b>. Multiple file names should be separated with spaces. A file name that contains spaces can be enclosed in quotation marks, for example, <b>"C:\\</b><i>My File</i><b>"</b>. In this case, it is treated as a single name. A caret  (^) can also be used as the quotation mechanism for single characters, for example, C:\My^"File and  "C:\My^"File" both refer to the file C:\My"File.

### -param nType [in]

Specifies the item type, which must be WNTYPE_FILE.

## -returns

If the function succeeds, it returns WN_SUCCESS. If the function fails, it returns an error code. Call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> to set this extended error code, which may include the following return codes.
					

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_VALUE</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters is an unexpected form or value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to display the dialog box.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network error occurred.

</td>
</tr>
</table>

## -remarks

This function is  called only on sets of properties for which 
<a href="/windows/desktop/api/npapi/nf-npapi-npgetpropertytext">NPGetPropertyText</a> has assigned a button name.

This function is used in File Manager to view and modify the network properties (for example, permissions) for files on a network device. If this function is not supported, File Manager does not provide any default behavior.

In this version of the Network Provider interface, <i>lpFileName</i> can point to only file names. The network provider should return WN_BAD_VALUE if it sees an inappropriate device.

## -see-also

<a href="/windows/desktop/api/npapi/nf-npapi-npgetpropertytext">NPGetPropertyText</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a>