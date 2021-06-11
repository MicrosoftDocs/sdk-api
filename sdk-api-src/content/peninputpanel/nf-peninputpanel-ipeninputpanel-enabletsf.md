---
UID: NF:peninputpanel.IPenInputPanel.EnableTsf
title: IPenInputPanel::EnableTsf (peninputpanel.h)
description: Deprecated. Gets or sets a Boolean value that indicates whether the PenInputPanel object attempts to send text to the attached control through the Text Services Framework (TSF) and enables the use of the correction user interface.
helpviewer_keywords: ["2c28e007-f06b-4d04-91a5-10e4b087fb2f","EnableTsf","EnableTsf method [Tablet PC]","EnableTsf method [Tablet PC]","IPenInputPanel interface","IPenInputPanel interface [Tablet PC]","EnableTsf method","IPenInputPanel.EnableTsf","IPenInputPanel::EnableTsf","peninputpanel/IPenInputPanel::EnableTsf","tablet.peninputpanel_enabletsf"]
old-location: tablet\peninputpanel_enabletsf.htm
tech.root: tablet
ms.assetid: 2c28e007-f06b-4d04-91a5-10e4b087fb2f
ms.date: 12/05/2018
ms.keywords: 2c28e007-f06b-4d04-91a5-10e4b087fb2f, EnableTsf, EnableTsf method [Tablet PC], EnableTsf method [Tablet PC],IPenInputPanel interface, IPenInputPanel interface [Tablet PC],EnableTsf method, IPenInputPanel.EnableTsf, IPenInputPanel::EnableTsf, peninputpanel/IPenInputPanel::EnableTsf, tablet.peninputpanel_enabletsf
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
 - IPenInputPanel::EnableTsf
 - peninputpanel/IPenInputPanel::EnableTsf
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
 - IPenInputPanel.EnableTsf
---

# IPenInputPanel::EnableTsf


## -description

<p class="CCE_Message">[  The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.]

Deprecated. Gets or sets a Boolean value that indicates whether the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object attempts to send text to the attached control through the <a href="/windows/desktop/TSF/text-services-framework">Text Services Framework</a> (TSF) and enables the use of the <b>correction</b> user interface.

## -parameters

### -param Enable

<b>TRUE</b> if the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object should attempt to send text to the attached control using TSF and that the correction user interface should be enabled; otherwise <b>FALSE</b>. The default value is <b>TRUE</b>.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
TSF interfaces are not exposed on the attached control.

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

Calling this method with Enable set to <b>TRUE</b> causes the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object to attempt to start the TSF on the attached control.

<b>EnableTsf</b> should be used to enable the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> to use the TSF insertion context rather than the <a href="/windows/desktop/api/winuser/nf-winuser-sendinput">SendInput</a> function to send the handwriting recognition results into the control. The result is that text can be inserted even if the field no longer has focus.

When you call <b>EnableTsf</b> with a value of <b>TRUE</b>, the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object sends an <a href="/windows/desktop/Controls/em-seteditstyle">EM_SETEDITSTYLE</a> message to the attached control. If the control does not support this message, results may be unpredictable. The <a href="/windows/desktop/tablet/inkedit-control">InkEdit</a> control does support TSF.

<h3><a id="Support_for_Legacy_Applications"></a><a id="support_for_legacy_applications"></a><a id="SUPPORT_FOR_LEGACY_APPLICATIONS"></a>Support for Legacy Applications</h3>
Support has been added to TSF and Microsoft Windows to provide a consistent user interface for all applications across the desktop. This new support enables legacy applications or controls that are not aware of TSF to take advantage of some advanced text services for free. For example, speech dictation and handwriting can now be used to enter text into a document in any application.

This new feature is available and enabled by default on Windows XP Tablet PC Edition. To enable or disable it:

<ol>
<li>
In Control Panel, click <b>Regional and Language Options</b>.

</li>
<li>
On the <b>Languages</b> tab, click <b>Details</b>.

</li>
<li>
On the <b>Advanced</b> tab of the <b>Text Services and Input Languages</b> dialog box, select or clear <b>Extend support of advanced text services to all programs</b>.

</li>
</ol>
If successful, text is sent to the attached control through TSF. Furthermore, if the control supports TSF (and is not simply receiving text from TSF just because Advanced Text Services has been enabled for all programs in Control Panel as noted above), then the correction user interface appears in the control and allows access to handwriting alternates. Calling this method with Enable set to <b>FALSE</b> causes the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object to attempt to shut down TSF on the attached control.

## -see-also

<a href="../peninputpanel/nn-peninputpanel-ipeninputpanel.md">IPenInputPanel</a>



<a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>
