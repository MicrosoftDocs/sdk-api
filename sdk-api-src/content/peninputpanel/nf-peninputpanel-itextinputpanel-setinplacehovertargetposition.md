---
UID: NF:peninputpanel.ITextInputPanel.SetInPlaceHoverTargetPosition
title: ITextInputPanel::SetInPlaceHoverTargetPosition (peninputpanel.h)
description: Explicitly positions the Tablet PC Input Panel hover target in screen coordinates.
helpviewer_keywords: ["1f007a76-8499-4128-8525-0498ddeb7300","ITextInputPanel interface [Tablet PC]","SetInPlaceHoverTargetPosition method","ITextInputPanel.SetInPlaceHoverTargetPosition","ITextInputPanel::SetInPlaceHoverTargetPosition","SetInPlaceHoverTargetPosition","SetInPlaceHoverTargetPosition method [Tablet PC]","SetInPlaceHoverTargetPosition method [Tablet PC]","ITextInputPanel interface","peninputpanel/ITextInputPanel::SetInPlaceHoverTargetPosition","tablet.itextinputpanel_setinplacehovertargetposition"]
old-location: tablet\itextinputpanel_setinplacehovertargetposition.htm
tech.root: tablet
ms.assetid: 1f007a76-8499-4128-8525-0498ddeb7300
ms.date: 12/05/2018
ms.keywords: 1f007a76-8499-4128-8525-0498ddeb7300, ITextInputPanel interface [Tablet PC],SetInPlaceHoverTargetPosition method, ITextInputPanel.SetInPlaceHoverTargetPosition, ITextInputPanel::SetInPlaceHoverTargetPosition, SetInPlaceHoverTargetPosition, SetInPlaceHoverTargetPosition method [Tablet PC], SetInPlaceHoverTargetPosition method [Tablet PC],ITextInputPanel interface, peninputpanel/ITextInputPanel::SetInPlaceHoverTargetPosition, tablet.itextinputpanel_setinplacehovertargetposition
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
 - ITextInputPanel::SetInPlaceHoverTargetPosition
 - peninputpanel/ITextInputPanel::SetInPlaceHoverTargetPosition
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
 - ITextInputPanel.SetInPlaceHoverTargetPosition
---

# ITextInputPanel::SetInPlaceHoverTargetPosition


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Explicitly positions the Tablet PC Input Panel hover target in screen coordinates.

## -parameters

### -param xPosition

The horizontal x-coordinate for the top left corner of the hover target, with no correction comb visible.

### -param yPosition

The vertical y-coordinate for the top left corner of the hover target, with no correction comb visible.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

There are no restrictions on where the hover target can be placed. The application is responsible for making sure the hover target stays on screen.

The <b>SetInPlaceHoverTargetPosition</b> method is synchronous. Positioning occurs before the method returns.


#### Examples

This C++ example implements an <code>EN_SETFOCUS</code> event handler for an Edit control, <code>IDC_EDIT2</code>. It first checks if an <a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> object, <code>g_pTip</code>, has been created. If it exists, it sets the position of the Input Panel hover target by calling the <b>ITextInputPanel::SetInPlaceHoverTargetPosition Method</b>. It then reports whether the call was successful to debug output using the <b>TRACE</b> macro.


```cpp
void CCOMTIPDlg::OnEnSetfocusEdit2()
{
	if (NULL != g_pTip)
	{
		if (SUCCEEDED(g_pTip->SetInPlaceHoverTargetPosition(300, 300)))
		{
			TRACE("Call to SetInPlaceHoverTargetPosition() succeeded.\n");
		}
		else
		{
			TRACE("Call to SetInPlaceHoverTargetPosition() failed.\n");
		}
	}
    else
    {
        TRACE("ITextInputPanel object is NULL.\n");
    }
}

```

## -see-also

<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel Interface</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplaceposition">ITextInputPanel::SetInPlacePosition Method</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplacevisibility">ITextInputPanel::SetInPlaceVisibility Method</a>