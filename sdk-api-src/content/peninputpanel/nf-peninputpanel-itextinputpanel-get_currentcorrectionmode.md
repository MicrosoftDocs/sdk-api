---
UID: NF:peninputpanel.ITextInputPanel.get_CurrentCorrectionMode
title: ITextInputPanel::get_CurrentCorrectionMode
author: windows-sdk-content
description: Gets the current correction comb mode as specified by the CorrectionMode Enumeration.
old-location: tablet\itextinputpanel_currentcorrectionmode.htm
old-project: tablet
ms.assetid: 92cd44a0-4dc6-4882-9ebb-45aa5b3fbc69
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: 92cd44a0-4dc6-4882-9ebb-45aa5b3fbc69, CurrentCorrectionMode property [Tablet PC], CurrentCorrectionMode property [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],CurrentCorrectionMode property, ITextInputPanel.CurrentCorrectionMode, ITextInputPanel.get_CurrentCorrectionMode, ITextInputPanel::CurrentCorrectionMode, ITextInputPanel::get_CurrentCorrectionMode, get_CurrentCorrectionMode, peninputpanel/ITextInputPanel::CurrentCorrectionMode, peninputpanel/ITextInputPanel::get_CurrentCorrectionMode, tablet.itextinputpanel_currentcorrectionmode
ms.prod: windows
ms.technology: windows-sdk
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
 - ITextInputPanel.CurrentCorrectionMode
 - ITextInputPanel.get_CurrentCorrectionMode
 - ITextInputPanel.get_CurrentCorrectionMode
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: ADAM
---

# ITextInputPanel::get_CurrentCorrectionMode


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Gets the current correction comb mode as specified by the <a href="https://msdn.microsoft.com/133d2012-e43c-490a-b126-b7670ea7acf8">CorrectionMode Enumeration</a>.



This property is read-only.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  
		In Windows 7, the behavior of the ITextInputPanel interface has changed and the <i>Mode</i> parameter will always be set to "no correction" when returned.
		</div>
<div> </div>
When the Tablet PC Input Panel or the correction comb is not visible, the current mode is <a href="https://msdn.microsoft.com/133d2012-e43c-490a-b126-b7670ea7acf8">CorrectionMode_NotVisible</a>.


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

		if (SUCCEEDED(g_pTip-&gt;get_CurrentCorrectionMode(&amp;mode)))
        {
			TRACE("CurrentCorrectionMode: %d\n", mode);
		}

		InPlaceState state;

		if (SUCCEEDED(g_pTip-&gt;get_CurrentInPlaceState(&amp;state)))
        {
			TRACE("CurrentInPlaceState: %d\n", state);
		}

		PanelInputArea area;

		if (SUCCEEDED(g_pTip-&gt;get_CurrentInputArea(&amp;area)))
        {
			TRACE("CurrentInputArea: %d\n", area);
		}

		InteractionMode iMode;

		if (SUCCEEDED(g_pTip-&gt;get_CurrentInteractionMode(&amp;iMode)))
        {
			TRACE("CurrentInteractionMode: %d\n", iMode);
		}

        RECT rect;

		if (SUCCEEDED(g_pTip-&gt;get_InPlaceBoundingRectangle(&amp;rect)))
        {
	        TRACE("InPlaceBoundingRectangle.top: %d\n", rect.top);
	        TRACE("InPlaceBoundingRectangle.left: %d\n", rect.left);
	        TRACE("InPlaceBoundingRectangle.bottom: %d\n", rect.bottom);
	        TRACE("InPlaceBoundingRectangle.right: %d\n", rect.right);
        }

	    int nHeight;

		if (SUCCEEDED(g_pTip-&gt;get_PopDownCorrectionHeight(&amp;nHeight)))
        {
	        TRACE("PopDownCorrectionHeight: %d\n", nHeight);
        }

	    if (SUCCEEDED(g_pTip-&gt;get_PopUpCorrectionHeight(&amp;nHeight)))
        {
	        TRACE("PopUpCorrectionHeight: %d\n", nHeight);
        }

		if (SUCCEEDED(g_pTip-&gt;SetInPlacePosition(300, 300, CorrectionPosition_Bottom)))
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
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>
 

 

