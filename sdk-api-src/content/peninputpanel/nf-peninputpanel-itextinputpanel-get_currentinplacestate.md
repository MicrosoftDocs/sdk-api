---
UID: NF:peninputpanel.ITextInputPanel.get_CurrentInPlaceState
title: ITextInputPanel::get_CurrentInPlaceState
author: windows-sdk-content
description: Gets the current in-place state as specified by the InPlaceState Enumeration.
old-location: tablet\itextinputpanel_currentinplacestate.htm
old-project: tablet
ms.assetid: 3ca27156-ed34-4cac-ba26-edded586272a
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: 3ca27156-ed34-4cac-ba26-edded586272a, CurrentInPlaceState property [Tablet PC], CurrentInPlaceState property [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],CurrentInPlaceState property, ITextInputPanel.CurrentInPlaceState, ITextInputPanel.get_CurrentInPlaceState, ITextInputPanel::CurrentInPlaceState, ITextInputPanel::get_CurrentInPlaceState, get_CurrentInPlaceState, peninputpanel/ITextInputPanel::CurrentInPlaceState, peninputpanel/ITextInputPanel::get_CurrentInPlaceState, tablet.itextinputpanel_currentinplacestate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: peninputpanel.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EventMask
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITextInputPanel.CurrentInPlaceState
 - ITextInputPanel.get_CurrentInPlaceState
 - ITextInputPanel.get_CurrentInPlaceState
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: ADAM
---

# ITextInputPanel::get_CurrentInPlaceState


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Gets the current in-place state as specified by the <a href="https://msdn.microsoft.com/95642cbf-4520-44cc-95ba-80de1fe3b447">InPlaceState Enumeration</a>.



This property is read-only.


## -parameters


## -remarks



When the Tablet PC Input Panel is closed or hidden, the current in-place state is reset to the default state, unless the default state is <a href="https://msdn.microsoft.com/95642cbf-4520-44cc-95ba-80de1fe3b447">Auto</a>, in which case, the current in-place state is reset to <b>Hover</b>.


#### Examples

This C++ example implements an <code>EN_SETFOCUS</code> event handler for an Edit control, <code>IDC_EDIT3</code>. It first checks if an <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> object, <code>g_pTip</code>, has been created. If it exists, it reports the values of several <b>ITextInputPanel Interface</b> properties to debug output using the <b>TRACE</b> macro.



<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void CCOMTIPDlg::OnEnSetFocusEdit3()
{
    if (NULL != g_pTip)
    {
		CorrectionMode mode;

		if (SUCCEEDED(g_pTip-&amp;gt;get_CurrentCorrectionMode(&amp;amp;mode)))
        {
			TRACE("CurrentCorrectionMode: %d\n", mode);
		}

		InPlaceState state;

		if (SUCCEEDED(g_pTip-&amp;gt;get_CurrentInPlaceState(&amp;amp;state)))
        {
			TRACE("CurrentInPlaceState: %d\n", state);
		}

		PanelInputArea area;

		if (SUCCEEDED(g_pTip-&amp;gt;get_CurrentInputArea(&amp;amp;area)))
        {
			TRACE("CurrentInputArea: %d\n", area);
		}

		InteractionMode iMode;

		if (SUCCEEDED(g_pTip-&amp;gt;get_CurrentInteractionMode(&amp;amp;iMode)))
        {
			TRACE("CurrentInteractionMode: %d\n", iMode);
		}

        RECT rect;

		if (SUCCEEDED(g_pTip-&amp;gt;get_InPlaceBoundingRectangle(&amp;amp;rect)))
        {
	        TRACE("InPlaceBoundingRectangle.top: %d\n", rect.top);
	        TRACE("InPlaceBoundingRectangle.left: %d\n", rect.left);
	        TRACE("InPlaceBoundingRectangle.bottom: %d\n", rect.bottom);
	        TRACE("InPlaceBoundingRectangle.right: %d\n", rect.right);
        }

	    int nHeight;

		if (SUCCEEDED(g_pTip-&amp;gt;get_PopDownCorrectionHeight(&amp;amp;nHeight)))
        {
	        TRACE("PopDownCorrectionHeight: %d\n", nHeight);
        }

	    if (SUCCEEDED(g_pTip-&amp;gt;get_PopUpCorrectionHeight(&amp;amp;nHeight)))
        {
	        TRACE("PopUpCorrectionHeight: %d\n", nHeight);
        }

		if (SUCCEEDED(g_pTip-&amp;gt;SetInPlacePosition(300, 300, CorrectionPosition_Bottom)))
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

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>
 

 

