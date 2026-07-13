---
UID: NF:peninputpanel.ITextInputPanel.put_PreferredInPlaceDirection
title: ITextInputPanel::put_PreferredInPlaceDirection (peninputpanel.h)
description: Gets or sets the preferred direction of the in-place Input Panel relative to the text entry field. (Put)
helpviewer_keywords: ["5d05e315-4e6d-4591-83d8-9cc98f2c2e2b","ITextInputPanel interface [Tablet PC]","PreferredInPlaceDirection property","ITextInputPanel.PreferredInPlaceDirection","ITextInputPanel.get_PreferredInPlaceDirection","ITextInputPanel.put_PreferredInPlaceDirection","ITextInputPanel::PreferredInPlaceDirection","ITextInputPanel::get_PreferredInPlaceDirection","ITextInputPanel::put_PreferredInPlaceDirection","PreferredInPlaceDirection property [Tablet PC]","PreferredInPlaceDirection property [Tablet PC]","ITextInputPanel interface","peninputpanel/ITextInputPanel::PreferredInPlaceDirection","peninputpanel/ITextInputPanel::get_PreferredInPlaceDirection","peninputpanel/ITextInputPanel::put_PreferredInPlaceDirection","put_PreferredInPlaceDirection","tablet.itextinputpanel_preferredinplacedirection"]
old-location: tablet\itextinputpanel_preferredinplacedirection.htm
tech.root: tablet
ms.assetid: 5d05e315-4e6d-4591-83d8-9cc98f2c2e2b
ms.date: 12/05/2018
ms.keywords: 5d05e315-4e6d-4591-83d8-9cc98f2c2e2b, ITextInputPanel interface [Tablet PC],PreferredInPlaceDirection property, ITextInputPanel.PreferredInPlaceDirection, ITextInputPanel.get_PreferredInPlaceDirection, ITextInputPanel.put_PreferredInPlaceDirection, ITextInputPanel::PreferredInPlaceDirection, ITextInputPanel::get_PreferredInPlaceDirection, ITextInputPanel::put_PreferredInPlaceDirection, PreferredInPlaceDirection property [Tablet PC], PreferredInPlaceDirection property [Tablet PC],ITextInputPanel interface, peninputpanel/ITextInputPanel::PreferredInPlaceDirection, peninputpanel/ITextInputPanel::get_PreferredInPlaceDirection, peninputpanel/ITextInputPanel::put_PreferredInPlaceDirection, put_PreferredInPlaceDirection, tablet.itextinputpanel_preferredinplacedirection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextInputPanel::put_PreferredInPlaceDirection
 - peninputpanel/ITextInputPanel::put_PreferredInPlaceDirection
dev_langs:
 - c++
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
---

# ITextInputPanel::put_PreferredInPlaceDirection


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Gets or sets the preferred direction of the in-place Input Panel relative to the text entry field.



This property is read/write.

## -parameters

## -remarks

An application can specify whether the in-place Input Panel defaults to appearing above or below a text entry field. To do this the application can set the <b>ITextInputPanel::PreferredInPlaceDirection Property</b> to <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-inplacedirection">InPlaceDirection_Bottom</a> or <b>InPlaceDirection_Top</b>. <b>ITextInputPanel::PreferredInPlaceDirection Property</b> is a preference because the in-place Input Panel overrides the preference set by the application when necessary to keep Input Panel on the screen. The system default is to position the in-place Input Panel below a text field when possible and otherwise to position it above. Setting the <b>PreferredInPlaceDirection</b> to <b>InPlaceDirection_Auto</b> restores the system default.


#### Examples

This C++ example creates an <a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> object, <code>g_pTip</code>, and attaches it to the window handle of an <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control, <code>IDC_EDIT3</code>, by setting the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_attachededitwindow">ITextInputPanel::AttachedEditWindow Property</a> property. It also sets, then gets the <b>ITextInputPanel::PreferredInPlaceDirection Property</b>.






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

<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel Interface</a>
