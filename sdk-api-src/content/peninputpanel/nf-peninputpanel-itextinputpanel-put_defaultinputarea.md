---
UID: NF:peninputpanel.ITextInputPanel.put_DefaultInputArea
title: ITextInputPanel::put_DefaultInputArea (peninputpanel.h)
description: Gets or sets the default input area as specified by the PanelInputArea Enumeration. (Put)
helpviewer_keywords: ["3e221516-631a-4d15-a9ef-bd05c6928067","DefaultInputArea property [Tablet PC]","DefaultInputArea property [Tablet PC]","ITextInputPanel interface","ITextInputPanel interface [Tablet PC]","DefaultInputArea property","ITextInputPanel.DefaultInputArea","ITextInputPanel.get_DefaultInputArea","ITextInputPanel.put_DefaultInputArea","ITextInputPanel::DefaultInputArea","ITextInputPanel::get_DefaultInputArea","ITextInputPanel::put_DefaultInputArea","peninputpanel/ITextInputPanel::DefaultInputArea","peninputpanel/ITextInputPanel::get_DefaultInputArea","peninputpanel/ITextInputPanel::put_DefaultInputArea","put_DefaultInputArea","tablet.itextinputpanel_defaultinputarea"]
old-location: tablet\itextinputpanel_defaultinputarea.htm
tech.root: tablet
ms.assetid: 3e221516-631a-4d15-a9ef-bd05c6928067
ms.date: 12/05/2018
ms.keywords: 3e221516-631a-4d15-a9ef-bd05c6928067, DefaultInputArea property [Tablet PC], DefaultInputArea property [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],DefaultInputArea property, ITextInputPanel.DefaultInputArea, ITextInputPanel.get_DefaultInputArea, ITextInputPanel.put_DefaultInputArea, ITextInputPanel::DefaultInputArea, ITextInputPanel::get_DefaultInputArea, ITextInputPanel::put_DefaultInputArea, peninputpanel/ITextInputPanel::DefaultInputArea, peninputpanel/ITextInputPanel::get_DefaultInputArea, peninputpanel/ITextInputPanel::put_DefaultInputArea, put_DefaultInputArea, tablet.itextinputpanel_defaultinputarea
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
 - ITextInputPanel::put_DefaultInputArea
 - peninputpanel/ITextInputPanel::put_DefaultInputArea
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
 - ITextInputPanel.DefaultInputArea
 - ITextInputPanel.get_DefaultInputArea
 - ITextInputPanel.put_DefaultInputArea
 - ITextInputPanel.get_DefaultInputArea
 - ITextInputPanel.put_DefaultInputArea
---

# ITextInputPanel::put_DefaultInputArea


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Gets or sets the default input area as specified by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-panelinputarea">PanelInputArea Enumeration</a>.



This property is read/write.

## -parameters

## -remarks

The system default is <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-panelinputarea">PanelInputArea_Auto</a>, except in password fields where the system default is <b>PanelInputArea_Keyboard</b>. Setting the default input area overrides the system default in all cases, except when an input area is unavailable because the current recognizer does not support that mode or because there is no recognizer for the current input language.


#### Examples

This C++ example creates an <a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> object, <code>g_pTip</code>, and attaches it to the window handle of an <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control, <code>IDC_EDIT3</code>, by setting the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_attachededitwindow">ITextInputPanel::AttachedEditWindow Property</a> property. It also sets, then gets the <b>ITextInputPanel::DefaultInputArea Property</b>.






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
