---
UID: NF:peninputpanel.ITextInputPanel.get_PopDownCorrectionHeight
title: ITextInputPanel::get_PopDownCorrectionHeight (peninputpanel.h)
description: Gets the height of the Post-Insertion correction comb when it is positioned below Input Panel.
helpviewer_keywords: ["525e5406-75ff-4f3c-a3f2-a542e04ca203","ITextInputPanel interface [Tablet PC]","PopDownCorrectionHeight property","ITextInputPanel.PopDownCorrectionHeight","ITextInputPanel.get_PopDownCorrectionHeight","ITextInputPanel::PopDownCorrectionHeight","ITextInputPanel::get_PopDownCorrectionHeight","PopDownCorrectionHeight property [Tablet PC]","PopDownCorrectionHeight property [Tablet PC]","ITextInputPanel interface","get_PopDownCorrectionHeight","peninputpanel/ITextInputPanel::PopDownCorrectionHeight","peninputpanel/ITextInputPanel::get_PopDownCorrectionHeight","tablet.itextinputpanel_popdowncorrectionheight"]
old-location: tablet\itextinputpanel_popdowncorrectionheight.htm
tech.root: tablet
ms.assetid: 525e5406-75ff-4f3c-a3f2-a542e04ca203
ms.date: 12/05/2018
ms.keywords: 525e5406-75ff-4f3c-a3f2-a542e04ca203, ITextInputPanel interface [Tablet PC],PopDownCorrectionHeight property, ITextInputPanel.PopDownCorrectionHeight, ITextInputPanel.get_PopDownCorrectionHeight, ITextInputPanel::PopDownCorrectionHeight, ITextInputPanel::get_PopDownCorrectionHeight, PopDownCorrectionHeight property [Tablet PC], PopDownCorrectionHeight property [Tablet PC],ITextInputPanel interface, get_PopDownCorrectionHeight, peninputpanel/ITextInputPanel::PopDownCorrectionHeight, peninputpanel/ITextInputPanel::get_PopDownCorrectionHeight, tablet.itextinputpanel_popdowncorrectionheight
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
 - ITextInputPanel::get_PopDownCorrectionHeight
 - peninputpanel/ITextInputPanel::get_PopDownCorrectionHeight
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
 - ITextInputPanel.PopDownCorrectionHeight
 - ITextInputPanel.get_PopDownCorrectionHeight
 - ITextInputPanel.get_PopDownCorrectionHeight
---

# ITextInputPanel::get_PopDownCorrectionHeight


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Gets the height of the Post-Insertion correction comb when it is positioned below Input Panel.



This property is read-only.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  In Windows 7, this function will always return the height as 0.
		</div>
<div> </div>
To get the full height of the in-place Input Panel with the Post-Insertion correction comb popped-down, add the height of the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_inplaceboundingrectangle">ITextInputPanel::InPlaceBoundingRectangle Property</a> to the <b>ITextInputPanel::PopDownCorrectionHeight Property</b>.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_popupcorrectionheight">ITextInputPanel::PopUpCorrectionHeight Property</a> is greater than or equal to the <b>ITextInputPanel::PopDownCorrectionHeight Property</b>.</div>
<div> </div>

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