---
UID: NF:peninputpanel.ITextInputPanel.get_DefaultInputArea
title: ITextInputPanel::get_DefaultInputArea
author: windows-sdk-content
description: Gets or sets the default input area as specified by the PanelInputArea Enumeration.
old-location: tablet\itextinputpanel_defaultinputarea.htm
old-project: tablet
ms.assetid: 3e221516-631a-4d15-a9ef-bd05c6928067
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 3e221516-631a-4d15-a9ef-bd05c6928067, DefaultInputArea property [Tablet PC], DefaultInputArea property [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],DefaultInputArea property, ITextInputPanel.DefaultInputArea, ITextInputPanel.get_DefaultInputArea, ITextInputPanel.put_DefaultInputArea, ITextInputPanel::DefaultInputArea, ITextInputPanel::get_DefaultInputArea, ITextInputPanel::put_DefaultInputArea, get_DefaultInputArea, peninputpanel/ITextInputPanel::DefaultInputArea, peninputpanel/ITextInputPanel::get_DefaultInputArea, peninputpanel/ITextInputPanel::put_DefaultInputArea, tablet.itextinputpanel_defaultinputarea
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
 - ITextInputPanel.DefaultInputArea
 - ITextInputPanel.get_DefaultInputArea
 - ITextInputPanel.put_DefaultInputArea
 - ITextInputPanel.get_DefaultInputArea
 - ITextInputPanel.put_DefaultInputArea
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: ADAM
---

# ITextInputPanel::get_DefaultInputArea


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Gets or sets the default input area as specified by the <a href="https://msdn.microsoft.com/fc262f07-aa73-49c8-a26a-1f0a47f8269a">PanelInputArea Enumeration</a>.



This property is read/write.


## -parameters


## -remarks



The system default is <a href="https://msdn.microsoft.com/fc262f07-aa73-49c8-a26a-1f0a47f8269a">PanelInputArea_Auto</a>, except in password fields where the system default is <b>PanelInputArea_Keyboard</b>. Setting the default input area overrides the system default in all cases, except when an input area is unavailable because the current recognizer does not support that mode or because there is no recognizer for the current input language.


#### Examples

This C++ example creates an <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> object, <code>g_pTip</code>, and attaches it to the window handle of an <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control, <code>IDC_EDIT3</code>, by setting the <a href="https://msdn.microsoft.com/92a8510d-c8f2-44b4-8812-789ddbc0e3fd">ITextInputPanel::AttachedEditWindow Property</a> property. It also sets, then gets the <b>ITextInputPanel::DefaultInputArea Property</b>.





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
 

 

