---
UID: NF:peninputpanel.ITextInputPanel.get_DefaultInPlaceState
title: ITextInputPanel::get_DefaultInPlaceState
author: windows-sdk-content
description: Gets or sets the default in-place state as specified by the InPlaceState Enumeration.
old-location: tablet\itextinputpanel_defaultinplacestate.htm
tech.root: tablet
ms.assetid: 00778a2c-9903-46a0-a5b3-c2ac4c355462
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 00778a2c-9903-46a0-a5b3-c2ac4c355462, DefaultInPlaceState property [Tablet PC], DefaultInPlaceState property [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],DefaultInPlaceState property, ITextInputPanel.DefaultInPlaceState, ITextInputPanel.get_DefaultInPlaceState, ITextInputPanel.put_DefaultInPlaceState, ITextInputPanel::DefaultInPlaceState, ITextInputPanel::get_DefaultInPlaceState, ITextInputPanel::put_DefaultInPlaceState, get_DefaultInPlaceState, peninputpanel/ITextInputPanel::DefaultInPlaceState, peninputpanel/ITextInputPanel::get_DefaultInPlaceState, peninputpanel/ITextInputPanel::put_DefaultInPlaceState, tablet.itextinputpanel_defaultinplacestate
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
 - ITextInputPanel.DefaultInPlaceState
 - ITextInputPanel.get_DefaultInPlaceState
 - ITextInputPanel.put_DefaultInPlaceState
 - ITextInputPanel.get_DefaultInPlaceState
 - ITextInputPanel.put_DefaultInPlaceState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextInputPanel::get_DefaultInPlaceState


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Gets or sets the default in-place state as specified by the <a href="https://msdn.microsoft.com/95642cbf-4520-44cc-95ba-80de1fe3b447">InPlaceState Enumeration</a>.



This property is read/write.


## -parameters


## -remarks



Set this property to <a href="https://msdn.microsoft.com/95642cbf-4520-44cc-95ba-80de1fe3b447">InPlaceState_Expanded</a> to have the Input Panel open without requiring the user to tap the hover target. Setting the default state to <b>InPlaceState_HoverTarget</b> overrides the Input Panel's heuristics for remaining expanded. When switching between fields, setting the default forces Input Panel to the collapsed or hover state, after a focus change. The system default is <b>InPlaceState_Auto</b>.


#### Examples

This C++ example creates an <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> object, <code>g_pTip</code>, and attaches it to the window handle of an <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control, <code>IDC_EDIT3</code>, by setting the <a href="https://msdn.microsoft.com/92a8510d-c8f2-44b4-8812-789ddbc0e3fd">ITextInputPanel::AttachedEditWindow Property</a> property. It also sets, then gets the <b>ITextInputPanel::DefaultInPlaceState Property</b>.




```cpp
if (SUCCEEDED(CoInitialize(NULL)))
{
    if (SUCCEEDED(CoCreateInstance(CLSID_TextInputPanel, NULL, CLSCTX_INPROC, IID_ITextInputPanel, (VOID**)&g_pTip)))
    {
        if (SUCCEEDED(g_pTip->put_AttachedEditWindow(GetDlgItem(IDC_EDIT3)->m_hWnd)))
        {
            g_pTip->put_DefaultInPlaceState(InPlaceState_Expanded);
            InPlaceState ips;
            g_pTip->get_DefaultInPlaceState(&ips);
            TRACE("DefaultInplaceState: %d\n", ips);
            
            g_pTip->put_DefaultInputArea(PanelInputArea_CharacterPad);
            PanelInputArea pia;
            g_pTip->get_DefaultInputArea(&pia);
            TRACE("DefaultInputArea: %d\n", pia);

            g_pTip->put_ExpandPostInsertionCorrection(FALSE);
            BOOL epic;
            g_pTip->get_ExpandPostInsertionCorrection(&epic);
            TRACE("ExpandPostInsertionCorrection: %d\n", epic);

            g_pTip->put_InPlaceVisibleOnFocus(TRUE);
            BOOL ipvof;
            g_pTip->get_InPlaceVisibleOnFocus(&ipvof);
            TRACE("InPlaceVisibleOnFocus: %d\n", ipvof);

            g_pTip->put_PreferredInPlaceDirection(InPlaceDirection_Top);
            InPlaceDirection direction;
            g_pTip->get_PreferredInPlaceDirection(&direction);
            TRACE("PreferredInPlaceDirection: %d\n", direction);
        }
    }
    else
    {
        TRACE("Failed to create ITextInputPanel object.\n");
    }
}

```





## -see-also




<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>
 

 

