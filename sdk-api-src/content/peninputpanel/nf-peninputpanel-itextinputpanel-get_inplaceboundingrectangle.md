---
UID: NF:peninputpanel.ITextInputPanel.get_InPlaceBoundingRectangle
title: ITextInputPanel::get_InPlaceBoundingRectangle
author: windows-sdk-content
description: Gets the bounding rectangle for Tablet PC Input Panel.
old-location: tablet\itextinputpanel_inplaceboundingrectangle.htm
tech.root: tablet
ms.assetid: 9a114f9d-b97d-4a2e-ac8e-f0a0241a6fbb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 9a114f9d-b97d-4a2e-ac8e-f0a0241a6fbb, ITextInputPanel interface [Tablet PC],InPlaceBoundingRectangle property, ITextInputPanel.InPlaceBoundingRectangle, ITextInputPanel.get_InPlaceBoundingRectangle, ITextInputPanel::InPlaceBoundingRectangle, ITextInputPanel::get_InPlaceBoundingRectangle, InPlaceBoundingRectangle property [Tablet PC], InPlaceBoundingRectangle property [Tablet PC],ITextInputPanel interface, get_InPlaceBoundingRectangle, peninputpanel/ITextInputPanel::InPlaceBoundingRectangle, peninputpanel/ITextInputPanel::get_InPlaceBoundingRectangle, tablet.itextinputpanel_inplaceboundingrectangle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- peninputpanel.h
: 
- ITextInputPanel.get_InPlaceBoundingRectangle
: 
---

# ITextInputPanel::get_InPlaceBoundingRectangle


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Gets the bounding rectangle for Tablet PC Input Panel.



This property is read-only.


## -parameters


## -remarks



If the Writing Pad or Character Pad is active, then the height of the Insert button is included in the bounding rectangle for the in-place Input Panel. The bounding rectangle does not include the height of the correction comb. When the in-place Input Panel auto grows, the <a href="https://msdn.microsoft.com/af9998a0-42ab-410d-980e-59a765d44667">ITextInputPanelEventSink::InPlaceSizeChanging Method</a>/<a href="https://msdn.microsoft.com/dd1f7cba-0a0f-49da-ad67-5c2e01830750">ITextInputPanelEventSink::InPlaceSizeChanged Method</a> event pair is fired and the value of this property is updated to include the additional writing area or writing line.


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
 

 

