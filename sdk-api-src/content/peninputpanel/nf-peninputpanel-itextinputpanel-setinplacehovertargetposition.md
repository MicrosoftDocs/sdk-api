---
UID: NF:peninputpanel.ITextInputPanel.SetInPlaceHoverTargetPosition
title: ITextInputPanel::SetInPlaceHoverTargetPosition
author: windows-sdk-content
description: Explicitly positions the Tablet PC Input Panel hover target in screen coordinates.
old-location: tablet\itextinputpanel_setinplacehovertargetposition.htm
tech.root: tablet
ms.assetid: 1f007a76-8499-4128-8525-0498ddeb7300
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: 1f007a76-8499-4128-8525-0498ddeb7300, ITextInputPanel interface [Tablet PC],SetInPlaceHoverTargetPosition method, ITextInputPanel.SetInPlaceHoverTargetPosition, ITextInputPanel::SetInPlaceHoverTargetPosition, SetInPlaceHoverTargetPosition, SetInPlaceHoverTargetPosition method [Tablet PC], SetInPlaceHoverTargetPosition method [Tablet PC],ITextInputPanel interface, peninputpanel/ITextInputPanel::SetInPlaceHoverTargetPosition, tablet.itextinputpanel_setinplacehovertargetposition
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
 - ITextInputPanel.SetInPlaceHoverTargetPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextInputPanel::SetInPlaceHoverTargetPosition


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Explicitly positions the Tablet PC Input Panel hover target in screen coordinates.




## -parameters




### -param xPosition

The horizontal x-coordinate for the top left corner of the hover target, with no correction comb visible.


### -param yPosition

The vertical y-coordinate for the top left corner of the hover target, with no correction comb visible.


## -returns



This method can return one of these values.

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



There are no restrictions on where the hover target can be placed. The application is responsible for making sure the hover target stays on screen.

The <b>SetInPlaceHoverTargetPosition</b> method is synchronous. Positioning occurs before the method returns.


#### Examples

This C++ example implements an <code>EN_SETFOCUS</code> event handler for an Edit control, <code>IDC_EDIT2</code>. It first checks if an <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> object, <code>g_pTip</code>, has been created. If it exists, it sets the position of the Input Panel hover target by calling the <b>ITextInputPanel::SetInPlaceHoverTargetPosition Method</b>. It then reports whether the call was successful to debug output using the <b>TRACE</b> macro.


```cpp
void CCOMTIPDlg::OnEnSetfocusEdit2()
{
	if (NULL != g_pTip)
	{
		if (SUCCEEDED(g_pTip->SetInPlaceHoverTargetPosition(300, 300)))
		{
			TRACE("Call to SetInPlaceHoverTargetPosition() succeeded.\n");
		}
		else
		{
			TRACE("Call to SetInPlaceHoverTargetPosition() failed.\n");
		}
	}
    else
    {
        TRACE("ITextInputPanel object is NULL.\n");
    }
}

```





## -see-also




<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>



<a href="https://msdn.microsoft.com/49bb1a89-7064-4822-866f-739434043869">ITextInputPanel::SetInPlacePosition Method</a>



<a href="https://msdn.microsoft.com/1e503857-9276-4308-b4ad-83db25866689">ITextInputPanel::SetInPlaceVisibility Method</a>
 

 

