---
UID: NF:peninputpanel.ITextInputPanel.get_CurrentCorrectionMode
title: ITextInputPanel::get_CurrentCorrectionMode (peninputpanel.h)
description: Gets the current correction comb mode as specified by the CorrectionMode Enumeration.
helpviewer_keywords: ["92cd44a0-4dc6-4882-9ebb-45aa5b3fbc69","CurrentCorrectionMode property [Tablet PC]","CurrentCorrectionMode property [Tablet PC]","ITextInputPanel interface","ITextInputPanel interface [Tablet PC]","CurrentCorrectionMode property","ITextInputPanel.CurrentCorrectionMode","ITextInputPanel.get_CurrentCorrectionMode","ITextInputPanel::CurrentCorrectionMode","ITextInputPanel::get_CurrentCorrectionMode","get_CurrentCorrectionMode","peninputpanel/ITextInputPanel::CurrentCorrectionMode","peninputpanel/ITextInputPanel::get_CurrentCorrectionMode","tablet.itextinputpanel_currentcorrectionmode"]
old-location: tablet\itextinputpanel_currentcorrectionmode.htm
tech.root: tablet
ms.assetid: 92cd44a0-4dc6-4882-9ebb-45aa5b3fbc69
ms.date: 12/05/2018
ms.keywords: 92cd44a0-4dc6-4882-9ebb-45aa5b3fbc69, CurrentCorrectionMode property [Tablet PC], CurrentCorrectionMode property [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],CurrentCorrectionMode property, ITextInputPanel.CurrentCorrectionMode, ITextInputPanel.get_CurrentCorrectionMode, ITextInputPanel::CurrentCorrectionMode, ITextInputPanel::get_CurrentCorrectionMode, get_CurrentCorrectionMode, peninputpanel/ITextInputPanel::CurrentCorrectionMode, peninputpanel/ITextInputPanel::get_CurrentCorrectionMode, tablet.itextinputpanel_currentcorrectionmode
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
 - ITextInputPanel::get_CurrentCorrectionMode
 - peninputpanel/ITextInputPanel::get_CurrentCorrectionMode
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
 - ITextInputPanel.CurrentCorrectionMode
 - ITextInputPanel.get_CurrentCorrectionMode
 - ITextInputPanel.get_CurrentCorrectionMode
---

# ITextInputPanel::get_CurrentCorrectionMode


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Gets the current correction comb mode as specified by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-correctionmode">CorrectionMode Enumeration</a>.



This property is read-only.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  In Windows 7, the behavior of the ITextInputPanel interface has changed and the <i>Mode</i> parameter will always be set to "no correction" when returned.
		</div>
<div> </div>
When the Tablet PC Input Panel or the correction comb is not visible, the current mode is <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-correctionmode">CorrectionMode_NotVisible</a>.


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