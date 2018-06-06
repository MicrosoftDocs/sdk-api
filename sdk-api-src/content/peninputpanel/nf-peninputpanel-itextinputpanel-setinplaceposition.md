---
UID: NF:peninputpanel.ITextInputPanel.SetInPlacePosition
title: ITextInputPanel::SetInPlacePosition
author: windows-sdk-content
description: Explicitly positions the Tablet PC Input Panel in screen coordinates.
old-location: tablet\itextinputpanel_setinplaceposition.htm
old-project: tablet
ms.assetid: 49bb1a89-7064-4822-866f-739434043869
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 49bb1a89-7064-4822-866f-739434043869, ITextInputPanel interface [Tablet PC],SetInPlacePosition method, ITextInputPanel.SetInPlacePosition, ITextInputPanel::SetInPlacePosition, SetInPlacePosition, SetInPlacePosition method [Tablet PC], SetInPlacePosition method [Tablet PC],ITextInputPanel interface, peninputpanel/ITextInputPanel::SetInPlacePosition, tablet.itextinputpanel_setinplaceposition
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
 - ITextInputPanel.SetInPlacePosition
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITextInputPanel::SetInPlacePosition


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Explicitly positions the Tablet PC Input Panel in screen coordinates.




## -parameters




### -param xPosition

The horizontal x-coordinate for the top left corner of the Input Panel, with no correction comb visible.


### -param yPosition

The vertical y-coordinate for the top left corner of the Input Panel, with no correction comb visible.


### -param position

The direction the post insertion correction comb should pop up in, as defined by the <a href="https://msdn.microsoft.com/0750128e-f3f0-444a-abe0-2dc360a3685b">CorrectionPosition</a> enumeration.


## -returns



Returns <b>false</b> when the Input Panel is open (docked or floating) and cannot be moved; otherwise it returns <b>true</b>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  
		In Windows 7, calling <b>SetInPlacePosition</b> will no longer use the <i>CorrectionPosition</i> parameter.
		</div>
<div> </div>
Take the height of the correction comb in mind when deciding where to position the Input Panel in order to keep the Input Panel and correction comb on screen. The direction specified in the <i>position</i> parameter overrides the direction set using the <a href="https://msdn.microsoft.com/5d05e315-4e6d-4591-83d8-9cc98f2c2e2b">ITextInputPanel::PreferredInPlaceDirection Property</a>.

There are no restrictions on where the Input Panel can be positioned. It is the responsibility of the application developer to make sure the Input Panel does not go off the screen. The <a href="https://msdn.microsoft.com/9a114f9d-b97d-4a2e-ac8e-f0a0241a6fbb">ITextInputPanel::InPlaceBoundingRectangle Property</a>, <a href="https://msdn.microsoft.com/986b7527-c634-45d9-a2eb-86fa999e57ba">ITextInputPanel::PopUpCorrectionHeight Property</a>, and <a href="https://msdn.microsoft.com/525e5406-75ff-4f3c-a3f2-a542e04ca203">ITextInputPanel::PopDownCorrectionHeight Property</a>, along with the <a href="https://msdn.microsoft.com/af9998a0-42ab-410d-980e-59a765d44667">ITextInputPanelEventSink::InPlaceSizeChanging Method</a>, can be used for this purpose.

This method is synchronous. Positioning occurs before the method returns.


#### Examples

This C++ example implements an <code>EN_SETFOCUS</code> event handler for an Edit control, <code>IDC_EDIT3</code>. It first checks to if an <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> object, <code>g_pTip</code>, has been created. If it exists, it reports the values of several <b>ITextInputPanel Interface</b> properties to debug output using the <b>TRACE</b> macro. It also sets the position of the Input Panel by calling the <b>ITextInputPanel::SetInPlacePosition Method</b>.

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
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>



<a href="https://msdn.microsoft.com/1f007a76-8499-4128-8525-0498ddeb7300">ITextInputPanel::SetInPlaceHoverTargetPosition Method</a>



<a href="https://msdn.microsoft.com/1e503857-9276-4308-b4ad-83db25866689">ITextInputPanel::SetInPlaceVisibility Method</a>
 

 

