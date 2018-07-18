---
UID: NF:peninputpanel.ITextInputPanel.get_AttachedEditWindow
title: ITextInputPanel::get_AttachedEditWindow
author: windows-sdk-content
description: Gets or sets the window handle of the object to which the ITextInputPanel object is attached.
old-location: tablet\itextinputpanel_attachededitwindow.htm
old-project: tablet
ms.assetid: 92a8510d-c8f2-44b4-8812-789ddbc0e3fd
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: 92a8510d-c8f2-44b4-8812-789ddbc0e3fd, AttachedEditWindow property [Tablet PC], AttachedEditWindow property [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],AttachedEditWindow property, ITextInputPanel.AttachedEditWindow, ITextInputPanel.get_AttachedEditWindow, ITextInputPanel.put_AttachedEditWindow, ITextInputPanel::AttachedEditWindow, ITextInputPanel::get_AttachedEditWindow, ITextInputPanel::put_AttachedEditWindow, get_AttachedEditWindow, peninputpanel/ITextInputPanel::AttachedEditWindow, peninputpanel/ITextInputPanel::get_AttachedEditWindow, peninputpanel/ITextInputPanel::put_AttachedEditWindow, tablet.itextinputpanel_attachededitwindow
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
 - ITextInputPanel.AttachedEditWindow
 - ITextInputPanel.get_AttachedEditWindow
 - ITextInputPanel.put_AttachedEditWindow
 - ITextInputPanel.get_AttachedEditWindow
 - ITextInputPanel.put_AttachedEditWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: ADAM
---

# ITextInputPanel::get_AttachedEditWindow


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Gets or sets the window handle of the object to which the <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> object is attached.



This property is read/write.


## -parameters


## -remarks



The window handle of an object may change.


#### Examples

This C++ example creates an <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> object, <code>g_pTip</code>, and attaches it to the window handle of an <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control, IDC_EDIT3, by setting the <b>ITextInputPanel::AttachedEditWindow Property</b> property.



<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>if (SUCCEEDED(CoInitialize(NULL)))
{
    if (SUCCEEDED(CoCreateInstance(CLSID_TextInputPanel, NULL, CLSCTX_INPROC, IID_ITextInputPanel, (VOID**)&amp;g_pTip)))
    {
        if (SUCCEEDED(g_pTip-&gt;put_AttachedEditWindow(GetDlgItem(IDC_EDIT3)-&gt;m_hWnd)))
        {
            g_pTip-&gt;put_DefaultInPlaceState(InPlaceState_Expanded);
            InPlaceState ips;
            g_pTip-&gt;get_DefaultInPlaceState(&amp;ips);
            TRACE("DefaultInplaceState: %d\n", ips);
            
            g_pTip-&gt;put_DefaultInputArea(PanelInputArea_CharacterPad);
            PanelInputArea pia;
            g_pTip-&gt;get_DefaultInputArea(&amp;pia);
            TRACE("DefaultInputArea: %d\n", pia);

            g_pTip-&gt;put_ExpandPostInsertionCorrection(FALSE);
            BOOL epic;
            g_pTip-&gt;get_ExpandPostInsertionCorrection(&amp;epic);
            TRACE("ExpandPostInsertionCorrection: %d\n", epic);

            g_pTip-&gt;put_InPlaceVisibleOnFocus(TRUE);
            BOOL ipvof;
            g_pTip-&gt;get_InPlaceVisibleOnFocus(&amp;ipvof);
            TRACE("InPlaceVisibleOnFocus: %d\n", ipvof);

            g_pTip-&gt;put_PreferredInPlaceDirection(InPlaceDirection_Top);
            InPlaceDirection direction;
            g_pTip-&gt;get_PreferredInPlaceDirection(&amp;direction);
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
 

 

