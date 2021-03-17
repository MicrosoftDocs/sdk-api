---
UID: NF:peninputpanel.ITextInputPanel.get_CurrentInteractionMode
title: ITextInputPanel::get_CurrentInteractionMode (peninputpanel.h)
description: Gets the positioning of the Tablet PC Input Panel as specified by the InteractionMode Enumeration.
helpviewer_keywords: ["CurrentInteractionMode property [Tablet PC]","CurrentInteractionMode property [Tablet PC]","ITextInputPanel interface","ITextInputPanel interface [Tablet PC]","CurrentInteractionMode property","ITextInputPanel.CurrentInteractionMode","ITextInputPanel.get_CurrentInteractionMode","ITextInputPanel::CurrentInteractionMode","ITextInputPanel::get_CurrentInteractionMode","dd28dad3-4b04-4597-9627-8fd27c75a207","get_CurrentInteractionMode","peninputpanel/ITextInputPanel::CurrentInteractionMode","peninputpanel/ITextInputPanel::get_CurrentInteractionMode","tablet.itextinputpanel_currentinteractionmode"]
old-location: tablet\itextinputpanel_currentinteractionmode.htm
tech.root: tablet
ms.assetid: dd28dad3-4b04-4597-9627-8fd27c75a207
ms.date: 12/05/2018
ms.keywords: CurrentInteractionMode property [Tablet PC], CurrentInteractionMode property [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],CurrentInteractionMode property, ITextInputPanel.CurrentInteractionMode, ITextInputPanel.get_CurrentInteractionMode, ITextInputPanel::CurrentInteractionMode, ITextInputPanel::get_CurrentInteractionMode, dd28dad3-4b04-4597-9627-8fd27c75a207, get_CurrentInteractionMode, peninputpanel/ITextInputPanel::CurrentInteractionMode, peninputpanel/ITextInputPanel::get_CurrentInteractionMode, tablet.itextinputpanel_currentinteractionmode
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
 - ITextInputPanel::get_CurrentInteractionMode
 - peninputpanel/ITextInputPanel::get_CurrentInteractionMode
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
 - ITextInputPanel.CurrentInteractionMode
 - ITextInputPanel.get_CurrentInteractionMode
 - ITextInputPanel.get_CurrentInteractionMode
---

# ITextInputPanel::get_CurrentInteractionMode


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Gets the positioning of the Tablet PC Input Panel as specified by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-interactionmode">InteractionMode Enumeration</a>.



This property is read-only.

## -parameters

## -remarks

The current interaction mode is dictated by the user. However, the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-interactionmode">InteractionMode_InPlace</a> mode can be disabled by the application on a per field basis.


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