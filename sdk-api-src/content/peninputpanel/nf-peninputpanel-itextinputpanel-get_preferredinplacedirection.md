---
UID: NF:peninputpanel.ITextInputPanel.get_PreferredInPlaceDirection
title: ITextInputPanel::get_PreferredInPlaceDirection
author: windows-sdk-content
description: Gets or sets the preferred direction of the in-place Input Panel relative to the text entry field.
old-location: tablet\itextinputpanel_preferredinplacedirection.htm
old-project: tablet
ms.assetid: 5d05e315-4e6d-4591-83d8-9cc98f2c2e2b
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: 5d05e315-4e6d-4591-83d8-9cc98f2c2e2b, ITextInputPanel interface [Tablet PC],PreferredInPlaceDirection property, ITextInputPanel.PreferredInPlaceDirection, ITextInputPanel.get_PreferredInPlaceDirection, ITextInputPanel.put_PreferredInPlaceDirection, ITextInputPanel::PreferredInPlaceDirection, ITextInputPanel::get_PreferredInPlaceDirection, ITextInputPanel::put_PreferredInPlaceDirection, PreferredInPlaceDirection property [Tablet PC], PreferredInPlaceDirection property [Tablet PC],ITextInputPanel interface, get_PreferredInPlaceDirection, peninputpanel/ITextInputPanel::PreferredInPlaceDirection, peninputpanel/ITextInputPanel::get_PreferredInPlaceDirection, peninputpanel/ITextInputPanel::put_PreferredInPlaceDirection, tablet.itextinputpanel_preferredinplacedirection
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
 - ITextInputPanel.PreferredInPlaceDirection
 - ITextInputPanel.get_PreferredInPlaceDirection
 - ITextInputPanel.put_PreferredInPlaceDirection
 - ITextInputPanel.get_PreferredInPlaceDirection
 - ITextInputPanel.put_PreferredInPlaceDirection
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: ADAM
---

# ITextInputPanel::get_PreferredInPlaceDirection


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Gets or sets the preferred direction of the in-place Input Panel relative to the text entry field.



This property is read/write.


## -parameters


## -remarks



An application can specify whether the in-place Input Panel defaults to appearing above or below a text entry field. To do this the application can set the <b>ITextInputPanel::PreferredInPlaceDirection Property</b> to <a href="https://msdn.microsoft.com/798ad6d8-de1c-49dc-87a1-86bb4f73603a">InPlaceDirection_Bottom</a> or <b>InPlaceDirection_Top</b>. <b>ITextInputPanel::PreferredInPlaceDirection Property</b> is a preference because the in-place Input Panel overrides the preference set by the application when necessary to keep Input Panel on the screen. The system default is to position the in-place Input Panel below a text field when possible and otherwise to position it above. Setting the <b>PreferredInPlaceDirection</b> to <b>InPlaceDirection_Auto</b> restores the system default.


#### Examples

This C++ example creates an <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> object, <code>g_pTip</code>, and attaches it to the window handle of an <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control, <code>IDC_EDIT3</code>, by setting the <a href="https://msdn.microsoft.com/92a8510d-c8f2-44b4-8812-789ddbc0e3fd">ITextInputPanel::AttachedEditWindow Property</a> property. It also sets, then gets the <b>ITextInputPanel::PreferredInPlaceDirection Property</b>.





<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>if (SUCCEEDED(CoInitialize(NULL)))
{
    if (SUCCEEDED(CoCreateInstance(CLSID_TextInputPanel, NULL, CLSCTX_INPROC, IID_ITextInputPanel, (VOID**)&amp;amp;g_pTip)))
    {
        if (SUCCEEDED(g_pTip-&amp;gt;put_AttachedEditWindow(GetDlgItem(IDC_EDIT3)-&amp;gt;m_hWnd)))
        {
            g_pTip-&amp;gt;put_DefaultInPlaceState(InPlaceState_Expanded);
            InPlaceState ips;
            g_pTip-&amp;gt;get_DefaultInPlaceState(&amp;amp;ips);
            TRACE("DefaultInplaceState: %d\n", ips);
            
            g_pTip-&amp;gt;put_DefaultInputArea(PanelInputArea_CharacterPad);
            PanelInputArea pia;
            g_pTip-&amp;gt;get_DefaultInputArea(&amp;amp;pia);
            TRACE("DefaultInputArea: %d\n", pia);

            g_pTip-&amp;gt;put_ExpandPostInsertionCorrection(FALSE);
            BOOL epic;
            g_pTip-&amp;gt;get_ExpandPostInsertionCorrection(&amp;amp;epic);
            TRACE("ExpandPostInsertionCorrection: %d\n", epic);

            g_pTip-&amp;gt;put_InPlaceVisibleOnFocus(TRUE);
            BOOL ipvof;
            g_pTip-&amp;gt;get_InPlaceVisibleOnFocus(&amp;amp;ipvof);
            TRACE("InPlaceVisibleOnFocus: %d\n", ipvof);

            g_pTip-&amp;gt;put_PreferredInPlaceDirection(InPlaceDirection_Top);
            InPlaceDirection direction;
            g_pTip-&amp;gt;get_PreferredInPlaceDirection(&amp;amp;direction);
            TRACE("PreferredInPlaceDirection: %d\n", direction);
        }
    }
    else
    {
        TRACE("Failed to create ITextInputPanel object.\n");
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>
 

 

