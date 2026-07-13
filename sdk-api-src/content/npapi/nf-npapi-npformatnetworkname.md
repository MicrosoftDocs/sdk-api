---
UID: NF:npapi.NPFormatNetworkName
title: NPFormatNetworkName function (npapi.h)
description: Formats a network name in a provider-specific format for display in a control.
helpviewer_keywords: ["NPFormatNetworkName","NPFormatNetworkName function [Security]","WNFMT_ABBREVIATED","WNFMT_INENUM","WNFMT_MULTILINE","_mnp_npformatnetworkname","npapi/NPFormatNetworkName","security.npformatnetworkname"]
old-location: security\npformatnetworkname.htm
tech.root: security
ms.assetid: a1d599fb-7b1c-4828-9cd7-bd520513f5be
ms.date: 12/05/2018
ms.keywords: NPFormatNetworkName, NPFormatNetworkName function [Security], WNFMT_ABBREVIATED, WNFMT_INENUM, WNFMT_MULTILINE, _mnp_npformatnetworkname, npapi/NPFormatNetworkName, security.npformatnetworkname
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
req.lib: davclnt.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NPFormatNetworkName
 - npapi/NPFormatNetworkName
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
 - NPFormatNetworkName
---

# NPFormatNetworkName function


## -description

Formats a network name in a provider-specific format for display in a control.

## -parameters

### -param lpRemoteName [in]

Pointer to the network name to format.

### -param lpFormattedName [out]

Pointer to a string that receives the formatted name.

### -param lpnLength [in, out]

Pointer to <b>DWORD</b> that specifies the size, in characters, of the <i>lpFormattedName</i> buffer. If the return value of this function is WN_MORE_DATA, <i>lpnLength</i> contains the required buffer size, in characters.

### -param dwFlags [in]

Bitfield that indicates the type of format being requested. This parameter can be one of the following values. 




						

						
					



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WNFMT_MULTILINE"></a><a id="wnfmt_multiline"></a><dl>
<dt><b>WNFMT_MULTILINE</b></dt>
</dl>
</td>
<td width="60%">
The provider should place  backslash n (\\n)  where line breaks should appear in the name. The full name should be expressed.

</td>
</tr>
<tr>
<td width="40%"><a id="WNFMT_ABBREVIATED"></a><a id="wnfmt_abbreviated"></a><dl>
<dt><b>WNFMT_ABBREVIATED</b></dt>
</dl>
</td>
<td width="60%">
The provider should shorten the network name so that the information most useful for the user will fit in the available space.

</td>
</tr>
</table>
 


In addition, the following flag, which acts as a modifier to the preceding flags, can be included by using a bitwise-<b>OR</b> operation.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WNFMT_INENUM"></a><a id="wnfmt_inenum"></a><dl>
<dt><b>WNFMT_INENUM</b></dt>
</dl>
</td>
<td width="60%">
The network name is presented in the context of an enumeration where the name of the "container" appears immediately before the network name in the enumeration. This allows network providers to remove redundant information from the formatted name, providing a less cluttered display for the user.

</td>
</tr>
</table>

### -param dwAveCharPerLine [in]

Specifies the average number of characters that will fit on a single line where the network name is being presented. Specifically, this value is defined as the width of the control divided by the <b>tmAveCharWidth</b> field of the 
<a href="/windows/desktop/api/wingdi/ns-wingdi-textmetrica">TEXTMETRIC</a> structure from the font used for display in the control.

## -returns

If the function succeeds, it should return WN_SUCCESS.
					

If the function fails, it should return the following value. All other errors will be ignored, and the unformatted network name will be used.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The input buffer is too small.

</td>
</tr>
</table>

## -remarks

This function allows network vendors to trim or modify network names before they are presented to the user. For example, in the common <b>Open</b> dialog box, the <b>Drives</b> combo box presents all connected resources and their associated network name. Before each item is displayed, <b>NPFormatNetworkName</b> is called, and the network provider has the option of editing the name so it will fit in the combo box. More important, the network provider can edit the name to present the most significant portion of the network name to the user.

Note that <b>NPFormatNetworkName</b> is not routed to each network provider like most of the other network provider functions are. Each network vendor need worry only about formatting their own network name. They can assume that only names produced by their network provider driver will be passed to <b>NPFormatNetworkName</b>.

The WNFMT_ flags are typically passed at various places in the user interface as described in the following table. No assumptions should be made about what flags are passed where; this table is provided solely to help each network vendor  decide the best method for modifying their network name.

<table>
<tr>
<th>Display location</th>
<th>WNFMT_
MULTILINE</th>
<th>WNFMT_
ABBREVIATED</th>
<th>WNFMT_
INENUM</th>
</tr>
<tr>
<td>
File Manager <b>Connection</b> dialog box, <b>Drive</b> combo box, selection. (The selection section of the combo box is the upper rectangle, above the list section, which displays the current selection.)

</td>
<td> </td>
<td>
X

</td>
<td> </td>
</tr>
<tr>
<td>
File Manager <b>Connection</b> dialog box, <b>Drive</b> combo box, list. (The list section of the combo box is the list box that appears below the selection portion of the combo box.)

</td>
<td>
X

</td>
<td> </td>
<td> </td>
</tr>
<tr>
<td>
File Manager, <b>Shared Directories</b> list.

</td>
<td> </td>
<td>
X

</td>
<td>
X

</td>
</tr>
<tr>
<td>
File Manager <b>Disconnect Network Drive</b> list.

</td>
<td>
X

</td>
<td> </td>
<td> </td>
</tr>
<tr>
<td>
File Manager, toolbar, combo box, selection.

</td>
<td> </td>
<td>
X

</td>
<td> </td>
</tr>
<tr>
<td>
File Manager, toolbar, combo box, list.

</td>
<td>
X

</td>
<td> </td>
<td> </td>
</tr>
<tr>
<td>
Common <b>Open</b> and <b>Save</b> dialog boxes, <b>Drive</b> combo box, selection.

</td>
<td> </td>
<td>
X

</td>
<td> </td>
</tr>
<tr>
<td>
Common <b>Open</b> and <b>Save</b> dialog boxes, <b>Drive</b> combo box, list.

</td>
<td> </td>
<td>
X

</td>
<td> </td>
</tr>
</table>