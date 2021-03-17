---
UID: NF:peninputpanel.ITextInputPanel.SetInPlaceVisibility
title: ITextInputPanel::SetInPlaceVisibility (peninputpanel.h)
description: Shows or hides the Tablet PC Input Panel.
helpviewer_keywords: ["1e503857-9276-4308-b4ad-83db25866689","ITextInputPanel interface [Tablet PC]","SetInPlaceVisibility method","ITextInputPanel.SetInPlaceVisibility","ITextInputPanel::SetInPlaceVisibility","SetInPlaceVisibility","SetInPlaceVisibility method [Tablet PC]","SetInPlaceVisibility method [Tablet PC]","ITextInputPanel interface","peninputpanel/ITextInputPanel::SetInPlaceVisibility","tablet.itextinputpanel_setinplacevisibility"]
old-location: tablet\itextinputpanel_setinplacevisibility.htm
tech.root: tablet
ms.assetid: 1e503857-9276-4308-b4ad-83db25866689
ms.date: 12/05/2018
ms.keywords: 1e503857-9276-4308-b4ad-83db25866689, ITextInputPanel interface [Tablet PC],SetInPlaceVisibility method, ITextInputPanel.SetInPlaceVisibility, ITextInputPanel::SetInPlaceVisibility, SetInPlaceVisibility, SetInPlaceVisibility method [Tablet PC], SetInPlaceVisibility method [Tablet PC],ITextInputPanel interface, peninputpanel/ITextInputPanel::SetInPlaceVisibility, tablet.itextinputpanel_setinplacevisibility
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
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextInputPanel::SetInPlaceVisibility
 - peninputpanel/ITextInputPanel::SetInPlaceVisibility
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITextInputPanel.SetInPlaceVisibility
---

# ITextInputPanel::SetInPlaceVisibility


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Shows or hides the Tablet PC Input Panel.

## -parameters

### -param Visible

<b>TRUE</b> to show the Input Panel; <b>FALSE</b> to hide the Input Panel.

## -returns

If the Input Panel can display, the method returns <b>S_OK</b>, otherwise <b>E_FAIL</b>. See the Remarks section for more information about when the Input Panel can and cannot be affected by the <b>ITextInputPanel::SetInPlaceVisibility Method</b>.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

The Input Panel is shown as specified by the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_currentinplacestate">ITextInputPanel::CurrentInPlaceState Property</a> property.

Calling <b>ITextInputPanel::SetInPlaceVisibility Method</b> with the <i>Visible</i> parameter set to <b>TRUE</b> will fail if the Input Panel is already visible.

If the user has disabled in-place mode from the Input Panel options dialog, calling <b>ITextInputPanel::SetInPlaceVisibility Method</b> will fail.

Any ink already in the Input Panel, when visibility changes, is automatically inserted.

This method does not change the value of <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_inplacevisibleonfocus">ITextInputPanel::InPlaceVisibleOnFocus Property</a>, and on the subsequent focus change, the behavior reverts to the behavior specified by the <b>ITextInputPanel::InPlaceVisibleOnFocus Property</b>.

The <b>ITextInputPanel::SetInPlaceVisibility Method</b> is a synchronous call. The Input Panel visibility will change before the call returns.


#### Examples

This C++ example implements an <code>EN_SETFOCUS</code> event handler for an Edit control, <code>IDC_EDIT1</code>. It first checks to if an <a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> object, <code>g_pTip</code>, has been created. If it exists, it prevents the Input Panel from showing by calling the <b>ITextInputPanel::SetInPlaceVisibility Method</b> with a value of <b>false</b> for the <i>Visible</i> parameter.


```cpp
void CCOMTIPDlg::OnEnSetfocusEdit1()
{
	if (NULL != g_pTip)
	{
		if (SUCCEEDED(g_pTip->SetInPlaceVisibility(false)))
		{
			TRACE("Successfully hid the Input Panel.\n");
		}
	}
}

```

## -see-also

<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel Interface</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_defaultinplacestate">ITextInputPanel::DefaultInPlaceState Property</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplacehovertargetposition">ITextInputPanel::SetInPlaceHoverTargetPosition Method</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplaceposition">ITextInputPanel::SetInPlacePosition Method</a>



<a href="/windows/win32/api/peninputpanel/ne-peninputpanel-inplacestate">InPlaceState Enumeration</a>