---
UID: NF:peninputpanel.ITextInputPanel.SetInPlacePosition
title: ITextInputPanel::SetInPlacePosition (peninputpanel.h)
description: Explicitly positions the Tablet PC Input Panel in screen coordinates.
helpviewer_keywords: ["49bb1a89-7064-4822-866f-739434043869","ITextInputPanel interface [Tablet PC]","SetInPlacePosition method","ITextInputPanel.SetInPlacePosition","ITextInputPanel::SetInPlacePosition","SetInPlacePosition","SetInPlacePosition method [Tablet PC]","SetInPlacePosition method [Tablet PC]","ITextInputPanel interface","peninputpanel/ITextInputPanel::SetInPlacePosition","tablet.itextinputpanel_setinplaceposition"]
old-location: tablet\itextinputpanel_setinplaceposition.htm
tech.root: tablet
ms.assetid: 49bb1a89-7064-4822-866f-739434043869
ms.date: 12/05/2018
ms.keywords: 49bb1a89-7064-4822-866f-739434043869, ITextInputPanel interface [Tablet PC],SetInPlacePosition method, ITextInputPanel.SetInPlacePosition, ITextInputPanel::SetInPlacePosition, SetInPlacePosition, SetInPlacePosition method [Tablet PC], SetInPlacePosition method [Tablet PC],ITextInputPanel interface, peninputpanel/ITextInputPanel::SetInPlacePosition, tablet.itextinputpanel_setinplaceposition
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
 - ITextInputPanel::SetInPlacePosition
 - peninputpanel/ITextInputPanel::SetInPlacePosition
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
 - ITextInputPanel.SetInPlacePosition
---

# ITextInputPanel::SetInPlacePosition


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Explicitly positions the Tablet PC Input Panel in screen coordinates.

## -parameters

### -param xPosition

The horizontal x-coordinate for the top left corner of the Input Panel, with no correction comb visible.

### -param yPosition

The vertical y-coordinate for the top left corner of the Input Panel, with no correction comb visible.

### -param position

The direction the post insertion correction comb should pop up in, as defined by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-correctionposition">CorrectionPosition</a> enumeration.

## -returns

Returns <b>false</b> when the Input Panel is open (docked or floating) and cannot be moved; otherwise it returns <b>true</b>.

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

<div class="alert"><b>Note</b>  In Windows 7, calling <b>SetInPlacePosition</b> will no longer use the <i>CorrectionPosition</i> parameter.
		</div>
<div> </div>
Take the height of the correction comb in mind when deciding where to position the Input Panel in order to keep the Input Panel and correction comb on screen. The direction specified in the <i>position</i> parameter overrides the direction set using the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_preferredinplacedirection">ITextInputPanel::PreferredInPlaceDirection Property</a>.

There are no restrictions on where the Input Panel can be positioned. It is the responsibility of the application developer to make sure the Input Panel does not go off the screen. The <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_inplaceboundingrectangle">ITextInputPanel::InPlaceBoundingRectangle Property</a>, <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_popupcorrectionheight">ITextInputPanel::PopUpCorrectionHeight Property</a>, and <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_popdowncorrectionheight">ITextInputPanel::PopDownCorrectionHeight Property</a>, along with the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacesizechanging">ITextInputPanelEventSink::InPlaceSizeChanging Method</a>, can be used for this purpose.

This method is synchronous. Positioning occurs before the method returns.


#### Examples

This C++ example implements an <code>EN_SETFOCUS</code> event handler for an Edit control, <code>IDC_EDIT3</code>. It first checks to if an <a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> object, <code>g_pTip</code>, has been created. If it exists, it reports the values of several <b>ITextInputPanel Interface</b> properties to debug output using the <b>TRACE</b> macro. It also sets the position of the Input Panel by calling the <b>ITextInputPanel::SetInPlacePosition Method</b>.


```cpp
void CCOMTIPDlg::OnEnSetFocusEdit3()
{
    if (NULL != g_pTip)
    {
		CorrectionMode mode;

		if (SUCCEEDED(g_pTip->get_CurrentCorrectionMode(&mode)))
        {
			TRACE("CurrentCorrectionMode: %d\n", mode);
		}

		InPlaceState state;

		if (SUCCEEDED(g_pTip->get_CurrentInPlaceState(&state)))
        {
			TRACE("CurrentInPlaceState: %d\n", state);
		}

		PanelInputArea area;

		if (SUCCEEDED(g_pTip->get_CurrentInputArea(&area)))
        {
			TRACE("CurrentInputArea: %d\n", area);
		}

		InteractionMode iMode;

		if (SUCCEEDED(g_pTip->get_CurrentInteractionMode(&iMode)))
        {
			TRACE("CurrentInteractionMode: %d\n", iMode);
		}

        RECT rect;

		if (SUCCEEDED(g_pTip->get_InPlaceBoundingRectangle(&rect)))
        {
	        TRACE("InPlaceBoundingRectangle.top: %d\n", rect.top);
	        TRACE("InPlaceBoundingRectangle.left: %d\n", rect.left);
	        TRACE("InPlaceBoundingRectangle.bottom: %d\n", rect.bottom);
	        TRACE("InPlaceBoundingRectangle.right: %d\n", rect.right);
        }

	    int nHeight;

		if (SUCCEEDED(g_pTip->get_PopDownCorrectionHeight(&nHeight)))
        {
	        TRACE("PopDownCorrectionHeight: %d\n", nHeight);
        }

	    if (SUCCEEDED(g_pTip->get_PopUpCorrectionHeight(&nHeight)))
        {
	        TRACE("PopUpCorrectionHeight: %d\n", nHeight);
        }

		if (SUCCEEDED(g_pTip->SetInPlacePosition(300, 300, CorrectionPosition_Bottom)))
		{
			TRACE("Call to SetInPlacePosition() succeeded.\n");
		}
		else
		{
			TRACE("Call to SetInPlacePosition() failed.\n");
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



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplacehovertargetposition">ITextInputPanel::SetInPlaceHoverTargetPosition Method</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-setinplacevisibility">ITextInputPanel::SetInPlaceVisibility Method</a>