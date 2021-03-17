---
UID: NF:peninputpanel.ITextInputPanel.get_PopUpCorrectionHeight
title: ITextInputPanel::get_PopUpCorrectionHeight (peninputpanel.h)
description: Gets the height of the Post-Insertion correction comb when it is positioned above Input Panel.
helpviewer_keywords: ["986b7527-c634-45d9-a2eb-86fa999e57ba","ITextInputPanel interface [Tablet PC]","PopUpCorrectionHeight property","ITextInputPanel.PopUpCorrectionHeight","ITextInputPanel.get_PopUpCorrectionHeight","ITextInputPanel::PopUpCorrectionHeight","ITextInputPanel::get_PopUpCorrectionHeight","PopUpCorrectionHeight property [Tablet PC]","PopUpCorrectionHeight property [Tablet PC]","ITextInputPanel interface","get_PopUpCorrectionHeight","peninputpanel/ITextInputPanel::PopUpCorrectionHeight","peninputpanel/ITextInputPanel::get_PopUpCorrectionHeight","tablet.itextinputpanel_popupcorrectionheight"]
old-location: tablet\itextinputpanel_popupcorrectionheight.htm
tech.root: tablet
ms.assetid: 986b7527-c634-45d9-a2eb-86fa999e57ba
ms.date: 12/05/2018
ms.keywords: 986b7527-c634-45d9-a2eb-86fa999e57ba, ITextInputPanel interface [Tablet PC],PopUpCorrectionHeight property, ITextInputPanel.PopUpCorrectionHeight, ITextInputPanel.get_PopUpCorrectionHeight, ITextInputPanel::PopUpCorrectionHeight, ITextInputPanel::get_PopUpCorrectionHeight, PopUpCorrectionHeight property [Tablet PC], PopUpCorrectionHeight property [Tablet PC],ITextInputPanel interface, get_PopUpCorrectionHeight, peninputpanel/ITextInputPanel::PopUpCorrectionHeight, peninputpanel/ITextInputPanel::get_PopUpCorrectionHeight, tablet.itextinputpanel_popupcorrectionheight
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
 - ITextInputPanel::get_PopUpCorrectionHeight
 - peninputpanel/ITextInputPanel::get_PopUpCorrectionHeight
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
 - ITextInputPanel.PopUpCorrectionHeight
 - ITextInputPanel.get_PopUpCorrectionHeight
 - ITextInputPanel.get_PopUpCorrectionHeight
---

# ITextInputPanel::get_PopUpCorrectionHeight


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Gets the height of the Post-Insertion correction comb when it is positioned above Input Panel.



This property is read-only.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  In Windows 7, this function will always return the height as 0.
		</div>
<div> </div>
To get the full height of the in-place Input Panel with the Post-Insertion correction comb popped-up, add the height of the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_inplaceboundingrectangle">ITextInputPanel::InPlaceBoundingRectangle Property</a> to the <b>ITextInputPanel::PopUpCorrectionHeight Property</b>.


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