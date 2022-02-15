---
UID: NF:peninputpanel.IPenInputPanel.Refresh
title: IPenInputPanel::Refresh (peninputpanel.h)
description: Refresh is no longer available for use as of Windows XP Tablet PC Edition.
helpviewer_keywords: ["7f135184-76cc-4636-8c20-db29ca7d5540","IPenInputPanel interface [Tablet PC]","Refresh method","IPenInputPanel.Refresh","IPenInputPanel::Refresh","Refresh","Refresh method [Tablet PC]","Refresh method [Tablet PC]","IPenInputPanel interface","peninputpanel/IPenInputPanel::Refresh","tablet.peninputpanel_refresh"]
old-location: tablet\peninputpanel_refresh.htm
tech.root: tablet
ms.assetid: 7f135184-76cc-4636-8c20-db29ca7d5540
ms.date: 12/05/2018
ms.keywords: 7f135184-76cc-4636-8c20-db29ca7d5540, IPenInputPanel interface [Tablet PC],Refresh method, IPenInputPanel.Refresh, IPenInputPanel::Refresh, Refresh, Refresh method [Tablet PC], Refresh method [Tablet PC],IPenInputPanel interface, peninputpanel/IPenInputPanel::Refresh, tablet.peninputpanel_refresh
req.header: peninputpanel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPenInputPanel::Refresh
 - peninputpanel/IPenInputPanel::Refresh
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IPenInputPanel.Refresh
---

# IPenInputPanel::Refresh


## -description

<p class="CCE_Message">[<b>Refresh</b> is no longer available for use as of Windows XP Tablet PC Edition. Instead, use <a href="/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.]

Updates and restores the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> properties based on Tablet PC Input Panel settings, automatically positions the pen input panel, and sets the user interface to the default panel.



## -returns

This method can return one of these values.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.
              

</td>
</tr>
</table>

## -remarks

The <b>Refresh</b> method restores the default panel. For example, if the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel">DefaultPanel</a> property is set to <a href="/windows/desktop/api/peninputpanel/ne-peninputpanel-paneltype">Keyboard</a> and the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel">CurrentPanel</a> property is set to <b>Handwriting</b>, the <b>Refresh</b> method sets the pen input panel to <b>Keyboard</b>. If the <b>DefaultPanel</b> property is set to <b>Default</b>, the <b>Refresh</b> method does not change the pen input panel.

The <b>Refresh</b> method automatically positions the pen input panel relative to the control to which it is attached.

The <b>Refresh</b> method updates the pen input panel using the Input Panel settings. For instance, you can make changes to the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object, and then call <b>Refresh</b> to restore the settings to those copied from the Input Panel.

The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object is updated automatically whenever the Input Panel settings change.

Calling <b>Refresh</b> while the pen input panel does not have focus will generate an error.

<div class="alert"><b>Note</b>  Normally, you won't need to call <b>Refresh</b> because all of the above is executed during activation of the pen input panel. However, if the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow">AutoShow</a> property is set to <b>FALSE</b>, you can disable activation of the pen input panel. Therefore, the <b>Refresh</b> method is needed.</div>
<div> </div>

## -see-also

<a href="../peninputpanel/nn-peninputpanel-ipeninputpanel.md">IPenInputPanel</a>



<a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>
