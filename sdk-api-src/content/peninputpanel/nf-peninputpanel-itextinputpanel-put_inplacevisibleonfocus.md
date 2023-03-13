---
UID: NF:peninputpanel.ITextInputPanel.put_InPlaceVisibleOnFocus
title: ITextInputPanel::put_InPlaceVisibleOnFocus (peninputpanel.h)
description: Gets or sets a value that indicates whether the Tablet PC Input Panel is displayed automatically when the window to which it is attached gets focus. (Put)
helpviewer_keywords: ["487ffcee-9df6-48db-8c84-e7e073b8a643","ITextInputPanel interface [Tablet PC]","InPlaceVisibleOnFocus property","ITextInputPanel.InPlaceVisibleOnFocus","ITextInputPanel.get_InPlaceVisibleOnFocus","ITextInputPanel.put_InPlaceVisibleOnFocus","ITextInputPanel::InPlaceVisibleOnFocus","ITextInputPanel::get_InPlaceVisibleOnFocus","ITextInputPanel::put_InPlaceVisibleOnFocus","InPlaceVisibleOnFocus property [Tablet PC]","InPlaceVisibleOnFocus property [Tablet PC]","ITextInputPanel interface","peninputpanel/ITextInputPanel::InPlaceVisibleOnFocus","peninputpanel/ITextInputPanel::get_InPlaceVisibleOnFocus","peninputpanel/ITextInputPanel::put_InPlaceVisibleOnFocus","put_InPlaceVisibleOnFocus","tablet.itextinputpanel_inplacevisibleonfocus"]
old-location: tablet\itextinputpanel_inplacevisibleonfocus.htm
tech.root: tablet
ms.assetid: 487ffcee-9df6-48db-8c84-e7e073b8a643
ms.date: 12/05/2018
ms.keywords: 487ffcee-9df6-48db-8c84-e7e073b8a643, ITextInputPanel interface [Tablet PC],InPlaceVisibleOnFocus property, ITextInputPanel.InPlaceVisibleOnFocus, ITextInputPanel.get_InPlaceVisibleOnFocus, ITextInputPanel.put_InPlaceVisibleOnFocus, ITextInputPanel::InPlaceVisibleOnFocus, ITextInputPanel::get_InPlaceVisibleOnFocus, ITextInputPanel::put_InPlaceVisibleOnFocus, InPlaceVisibleOnFocus property [Tablet PC], InPlaceVisibleOnFocus property [Tablet PC],ITextInputPanel interface, peninputpanel/ITextInputPanel::InPlaceVisibleOnFocus, peninputpanel/ITextInputPanel::get_InPlaceVisibleOnFocus, peninputpanel/ITextInputPanel::put_InPlaceVisibleOnFocus, put_InPlaceVisibleOnFocus, tablet.itextinputpanel_inplacevisibleonfocus
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
 - ITextInputPanel::put_InPlaceVisibleOnFocus
 - peninputpanel/ITextInputPanel::put_InPlaceVisibleOnFocus
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
 - ITextInputPanel.InPlaceVisibleOnFocus
 - ITextInputPanel.get_InPlaceVisibleOnFocus
 - ITextInputPanel.put_InPlaceVisibleOnFocus
 - ITextInputPanel.get_InPlaceVisibleOnFocus
 - ITextInputPanel.put_InPlaceVisibleOnFocus
---

# ITextInputPanel::put_InPlaceVisibleOnFocus


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Gets or sets a value that indicates whether the Tablet PC Input Panel is displayed automatically when the window to which it is attached gets focus.



This property is read/write.

## -parameters

## -remarks

If <b>ITextInputPanel::InPlaceVisibleOnFocus Property</b> is set to <b>TRUE</b> for a control, then when the control gains focus, the Tablet PC Input Panel automatically shows in the default <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-inplacestate">InPlaceState Enumeration</a> provided it is a legal operation.

It is possible to prevent the in-place Input Panel and the Input Panel Icon from ever appearing by setting the <b>ITextInputPanel::InPlaceVisibleOnFocus Property</b> to <b>FALSE</b>. Setting it to <b>TRUE</b> reverts it to the system default of appearing when possible, provided it has not been disabled by the user or Group Policy. This option is useful for applications that include custom text entry solutions as an alternative to the Input Panel.

The default value is <b>TRUE</b>.


#### Examples

This C++ example creates an <a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> object, <code>g_pTip</code>, and attaches it to the window handle of an <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control, <code>IDC_EDIT3</code>, by setting the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_attachededitwindow">ITextInputPanel::AttachedEditWindow Property</a> property. It also sets, then gets the<b> ITextInputPanel::InPlaceVisibleOnFocus Property</b>.






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
