---
UID: NF:peninputpanel.ITextInputPanel.SetInPlaceVisibility
title: ITextInputPanel::SetInPlaceVisibility
author: windows-sdk-content
description: Shows or hides the Tablet PC Input Panel.
old-location: tablet\itextinputpanel_setinplacevisibility.htm
old-project: tablet
ms.assetid: 1e503857-9276-4308-b4ad-83db25866689
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 1e503857-9276-4308-b4ad-83db25866689, ITextInputPanel interface [Tablet PC],SetInPlaceVisibility method, ITextInputPanel.SetInPlaceVisibility, ITextInputPanel::SetInPlaceVisibility, SetInPlaceVisibility, SetInPlaceVisibility method [Tablet PC], SetInPlaceVisibility method [Tablet PC],ITextInputPanel interface, peninputpanel/ITextInputPanel::SetInPlaceVisibility, tablet.itextinputpanel_setinplacevisibility
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tiptsf.dll
api_name:
-	ITextInputPanel.SetInPlaceVisibility
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITextInputPanel::SetInPlaceVisibility


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Shows or hides the Tablet PC Input Panel.




## -parameters




### -param Visible

<b>TRUE</b> to show the Input Panel; <b>FALSE</b> to hide the Input Panel.


## -returns



If the Input Panel can display, the method returns <b>S_OK</b>, otherwise <b>E_FAIL</b>. See the Remarks section for more information about when the Input Panel can and cannot be affected by the <b>ITextInputPanel::SetInPlaceVisibility Method</b>.

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



The Input Panel is shown as specified by the <a href="https://msdn.microsoft.com/3ca27156-ed34-4cac-ba26-edded586272a">ITextInputPanel::CurrentInPlaceState Property</a> property.

Calling <b>ITextInputPanel::SetInPlaceVisibility Method</b> with the <i>Visible</i> parameter set to <b>TRUE</b> will fail if the Input Panel is already visible.

If the user has disabled in-place mode from the Input Panel options dialog, calling <b>ITextInputPanel::SetInPlaceVisibility Method</b> will fail.

Any ink already in the Input Panel, when visibility changes, is automatically inserted.

This method does not change the value of <a href="https://msdn.microsoft.com/487ffcee-9df6-48db-8c84-e7e073b8a643">ITextInputPanel::InPlaceVisibleOnFocus Property</a>, and on the subsequent focus change, the behavior reverts to the behavior specified by the <b>ITextInputPanel::InPlaceVisibleOnFocus Property</b>.

The <b>ITextInputPanel::SetInPlaceVisibility Method</b> is a synchronous call. The Input Panel visibility will change before the call returns.


#### Examples

This C++ example implements an <code>EN_SETFOCUS</code> event handler for an Edit control, <code>IDC_EDIT1</code>. It first checks to if an <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> object, <code>g_pTip</code>, has been created. If it exists, it prevents the Input Panel from showing by calling the <b>ITextInputPanel::SetInPlaceVisibility Method</b> with a value of <b>false</b> for the <i>Visible</i> parameter.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void CCOMTIPDlg::OnEnSetfocusEdit1()
{
	if (NULL != g_pTip)
	{
		if (SUCCEEDED(g_pTip-&gt;SetInPlaceVisibility(false)))
		{
			TRACE("Successfully hid the Input Panel.\n");
		}
	}
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>



<a href="https://msdn.microsoft.com/00778a2c-9903-46a0-a5b3-c2ac4c355462">ITextInputPanel::DefaultInPlaceState Property</a>



<a href="https://msdn.microsoft.com/1f007a76-8499-4128-8525-0498ddeb7300">ITextInputPanel::SetInPlaceHoverTargetPosition Method</a>



<a href="https://msdn.microsoft.com/49bb1a89-7064-4822-866f-739434043869">ITextInputPanel::SetInPlacePosition Method</a>



<a href="https://msdn.microsoft.com/95642cbf-4520-44cc-95ba-80de1fe3b447">InPlaceState Enumeration</a>
 

 

