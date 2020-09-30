---
UID: NF:peninputpanel.ITextInputPanel.get_InPlaceBoundingRectangle
title: ITextInputPanel::get_InPlaceBoundingRectangle (peninputpanel.h)
description: Gets the bounding rectangle for Tablet PC Input Panel.
helpviewer_keywords: ["9a114f9d-b97d-4a2e-ac8e-f0a0241a6fbb","ITextInputPanel interface [Tablet PC]","InPlaceBoundingRectangle property","ITextInputPanel.InPlaceBoundingRectangle","ITextInputPanel.get_InPlaceBoundingRectangle","ITextInputPanel::InPlaceBoundingRectangle","ITextInputPanel::get_InPlaceBoundingRectangle","InPlaceBoundingRectangle property [Tablet PC]","InPlaceBoundingRectangle property [Tablet PC]","ITextInputPanel interface","get_InPlaceBoundingRectangle","peninputpanel/ITextInputPanel::InPlaceBoundingRectangle","peninputpanel/ITextInputPanel::get_InPlaceBoundingRectangle","tablet.itextinputpanel_inplaceboundingrectangle"]
old-location: tablet\itextinputpanel_inplaceboundingrectangle.htm
tech.root: tablet
ms.assetid: 9a114f9d-b97d-4a2e-ac8e-f0a0241a6fbb
ms.date: 12/05/2018
ms.keywords: 9a114f9d-b97d-4a2e-ac8e-f0a0241a6fbb, ITextInputPanel interface [Tablet PC],InPlaceBoundingRectangle property, ITextInputPanel.InPlaceBoundingRectangle, ITextInputPanel.get_InPlaceBoundingRectangle, ITextInputPanel::InPlaceBoundingRectangle, ITextInputPanel::get_InPlaceBoundingRectangle, InPlaceBoundingRectangle property [Tablet PC], InPlaceBoundingRectangle property [Tablet PC],ITextInputPanel interface, get_InPlaceBoundingRectangle, peninputpanel/ITextInputPanel::InPlaceBoundingRectangle, peninputpanel/ITextInputPanel::get_InPlaceBoundingRectangle, tablet.itextinputpanel_inplaceboundingrectangle
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
 - ITextInputPanel::get_InPlaceBoundingRectangle
 - peninputpanel/ITextInputPanel::get_InPlaceBoundingRectangle
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
 - ITextInputPanel.InPlaceBoundingRectangle
 - ITextInputPanel.get_InPlaceBoundingRectangle
 - ITextInputPanel.get_InPlaceBoundingRectangle
---

# ITextInputPanel::get_InPlaceBoundingRectangle


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Gets the bounding rectangle for Tablet PC Input Panel.



This property is read-only.

## -parameters

## -remarks

If the Writing Pad or Character Pad is active, then the height of the Insert button is included in the bounding rectangle for the in-place Input Panel. The bounding rectangle does not include the height of the correction comb. When the in-place Input Panel auto grows, the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacesizechanging">ITextInputPanelEventSink::InPlaceSizeChanging Method</a>/<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacesizechanged">ITextInputPanelEventSink::InPlaceSizeChanged Method</a> event pair is fired and the value of this property is updated to include the additional writing area or writing line.


#### Examples

This C++ example implements an <code>EN_SETFOCUS</code> event handler for an Edit control, <code>IDC_EDIT3</code>. It first checks if an <a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> object, <code>g_pTip</code>, has been created. If it exists, it reports the values of several <b>ITextInputPanel Interface</b> properties to debug output using the <b>TRACE</b> macro.




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