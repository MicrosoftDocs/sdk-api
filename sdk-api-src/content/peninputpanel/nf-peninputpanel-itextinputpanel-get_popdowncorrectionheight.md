---
UID: NF:peninputpanel.ITextInputPanel.get_PopDownCorrectionHeight
title: ITextInputPanel::get_PopDownCorrectionHeight
author: windows-driver-content
description: Gets the height of the Post-Insertion correction comb when it is positioned below Input Panel.
old-location: tablet\itextinputpanel_popdowncorrectionheight.htm
old-project: tablet
ms.assetid: 525e5406-75ff-4f3c-a3f2-a542e04ca203
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: 525e5406-75ff-4f3c-a3f2-a542e04ca203, ITextInputPanel interface [Tablet PC],PopDownCorrectionHeight property, ITextInputPanel.PopDownCorrectionHeight, ITextInputPanel.get_PopDownCorrectionHeight, ITextInputPanel::PopDownCorrectionHeight, ITextInputPanel::get_PopDownCorrectionHeight, PopDownCorrectionHeight property [Tablet PC], PopDownCorrectionHeight property [Tablet PC],ITextInputPanel interface, get_PopDownCorrectionHeight, peninputpanel/ITextInputPanel::PopDownCorrectionHeight, peninputpanel/ITextInputPanel::get_PopDownCorrectionHeight, tablet.itextinputpanel_popdowncorrectionheight
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
req.typenames: EventMask
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tiptsf.dll
api_name:
-	ITextInputPanel.PopDownCorrectionHeight
-	ITextInputPanel.get_PopDownCorrectionHeight
-	ITextInputPanel.get_PopDownCorrectionHeight
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITextInputPanel::get_PopDownCorrectionHeight


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Gets the height of the Post-Insertion correction comb when it is positioned below Input Panel.



This property is read-only.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  
		In Windows 7, this function will always return the height as 0.
		</div>
<div> </div>
To get the full height of the in-place Input Panel with the Post-Insertion correction comb popped-down, add the height of the <a href="https://msdn.microsoft.com/9a114f9d-b97d-4a2e-ac8e-f0a0241a6fbb">ITextInputPanel::InPlaceBoundingRectangle Property</a> to the <b>ITextInputPanel::PopDownCorrectionHeight Property</b>.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/986b7527-c634-45d9-a2eb-86fa999e57ba">ITextInputPanel::PopUpCorrectionHeight Property</a> is greater than or equal to the <b>ITextInputPanel::PopDownCorrectionHeight Property</b>.</div>
<div> </div>

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
 

 

