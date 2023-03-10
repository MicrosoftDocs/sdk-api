---
UID: NE:shobjidl_core.tagDESKBANDCID
title: tagDESKBANDCID (shobjidl_core.h)
description: These command IDs can be sent to the band object's container with IOleCommandTarget::Exec.
helpviewer_keywords: ["DBID Command Flags","DBID_BANDINFOCHANGED","DBID_MAXIMIZEBAND","DBID_PUSHCHEVRON","DBID_SHOWONLY","shell.DBID_Command_Flags","shell_DBID_Command_Flags","shobjidl_core/DBID_BANDINFOCHANGED","shobjidl_core/DBID_MAXIMIZEBAND","shobjidl_core/DBID_PUSHCHEVRON","shobjidl_core/DBID_SHOWONLY","shobjidl_core/tagDESKBANDCID","tagDESKBANDCID","tagDESKBANDCID enumeration [Windows Shell]"]
old-location: shell\DBID_Command_Flags.htm
tech.root: shell
ms.assetid: 388e94de-a5c2-470e-ad33-dec3cfca2604
ms.date: 12/05/2018
ms.keywords: DBID Command Flags, DBID_BANDINFOCHANGED, DBID_MAXIMIZEBAND, DBID_PUSHCHEVRON, DBID_SHOWONLY, shell.DBID_Command_Flags, shell_DBID_Command_Flags, shobjidl_core/DBID_BANDINFOCHANGED, shobjidl_core/DBID_MAXIMIZEBAND, shobjidl_core/DBID_PUSHCHEVRON, shobjidl_core/DBID_SHOWONLY, shobjidl_core/tagDESKBANDCID, tagDESKBANDCID, tagDESKBANDCID enumeration [Windows Shell]
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDESKBANDCID
 - shobjidl_core/tagDESKBANDCID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - tagDESKBANDCID
---

# tagDESKBANDCID enumeration


## -description

These command IDs can be sent to the band object's container with <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec">IOleCommandTarget::Exec</a>.

## -enum-fields

### -field DBID_BANDINFOCHANGED:0

Updates all bands or a specific band.
				

<ul>
<li><b>To update all bands:</b> Set <i>pvaIn</i> to <b>NULL</b>.</li>
<li><b>To update a specific band:</b> Set <i>pvaIn-&gt;lVal</i> to the ID of the band to be updated, and <i>pvaIn-&gt;vt</i> to VT_I4.</li>
</ul>

### -field DBID_SHOWONLY:1

Turns other bands in the container on or off. Set <i>pvaIn-&gt;vt</i> to VT_UNKNOWN, and set <i>pvaIn-&gt;punkVal</i> to one of the following values.

				

<table class="clsStd">
<tr>
<th>Value</th>
<th>Result</th>
</tr>
<tr>
<td>pUnk</td>
<td>A pointer to the band object's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. The desk band pointed to is shown; all other desk bands are hidden.</td>
</tr>
<tr>
<td>0</td>
<td>Hides all desk bands.</td>
</tr>
<tr>
<td>1</td>
<td>Shows all desk bands.</td>
</tr>
</table>

### -field DBID_MAXIMIZEBAND:2

Maximize the band. Set <i>pvaIn-&gt;ulVal</i> to the ID of the band to be maximized, and set <i>pvaIn-&gt;vt</i> to VT_UI4.

### -field DBID_PUSHCHEVRON:3

<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5</a>. Displays a push chevron on a desk band. Set <i>pvaIn-&gt;vt</i> to VT_I4, set <i>pvaIn-&gt;lVal</i> to the ID of the desk band, and set the <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec">IOleCommandTarget::Exec</a> method's <i>nCmdExecOpt</i> parameter to the band identifier received in the most recent call to IDeskBand::GetBandInfo.  The container sends an RB_PUSHCHEVRON message, and the band object receives an RBN_CHEVRONPUSHED notification that prompts it to display the chevron. The band ID is passed back to the band object in the lParam parameter of the RBN_CHEVRONPUSHED message.

### -field DBID_DELAYINIT:4

### -field DBID_FINISHINIT:5

### -field DBID_SETWINDOWTHEME:6

### -field DBID_PERMITAUTOHIDE:7

## -remarks

Set the <i>pguidCmdGroup</i> parameter of the <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec">IOleCommandTarget::Exec</a> method to CGID_DeskBand, the <i>pvaIn</i> parameter to the value indicated in the command description, and the <i>nCmdID</i> parameter to one of the command values listed above.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)">Creating Custom Explorer Bars, Tool Bands, and Desk Bands</a>
