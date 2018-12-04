---
UID: NF:peninputpanel.ITextInputPanel.get_CurrentInteractionMode
title: ITextInputPanel::get_CurrentInteractionMode
author: windows-sdk-content
description: Gets the positioning of the Tablet PC Input Panel as specified by the InteractionMode Enumeration.
old-location: tablet\itextinputpanel_currentinteractionmode.htm
tech.root: tablet
ms.assetid: dd28dad3-4b04-4597-9627-8fd27c75a207
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CurrentInteractionMode property [Tablet PC], CurrentInteractionMode property [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],CurrentInteractionMode property, ITextInputPanel.CurrentInteractionMode, ITextInputPanel.get_CurrentInteractionMode, ITextInputPanel::CurrentInteractionMode, ITextInputPanel::get_CurrentInteractionMode, dd28dad3-4b04-4597-9627-8fd27c75a207, get_CurrentInteractionMode, peninputpanel/ITextInputPanel::CurrentInteractionMode, peninputpanel/ITextInputPanel::get_CurrentInteractionMode, tablet.itextinputpanel_currentinteractionmode
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
 - ITextInputPanel.CurrentInteractionMode
 - ITextInputPanel.get_CurrentInteractionMode
 - ITextInputPanel.get_CurrentInteractionMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextInputPanel::get_CurrentInteractionMode


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Gets the positioning of the Tablet PC Input Panel as specified by the <a href="https://msdn.microsoft.com/8e01c1fd-3351-47f1-beae-c84d9f7969a8">InteractionMode Enumeration</a>.



This property is read-only.


## -parameters


## -remarks



The current interaction mode is dictated by the user. However, the <a href="https://msdn.microsoft.com/8e01c1fd-3351-47f1-beae-c84d9f7969a8">InteractionMode_InPlace</a> mode can be disabled by the application on a per field basis.


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
 

 

