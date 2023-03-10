---
UID: NF:peninputpanel.ITextInputPanel.get_AttachedEditWindow
title: ITextInputPanel::get_AttachedEditWindow (peninputpanel.h)
description: Gets or sets the window handle of the object to which the ITextInputPanel object is attached. (Get)
helpviewer_keywords: ["92a8510d-c8f2-44b4-8812-789ddbc0e3fd","AttachedEditWindow property [Tablet PC]","AttachedEditWindow property [Tablet PC]","ITextInputPanel interface","ITextInputPanel interface [Tablet PC]","AttachedEditWindow property","ITextInputPanel.AttachedEditWindow","ITextInputPanel.get_AttachedEditWindow","ITextInputPanel.put_AttachedEditWindow","ITextInputPanel::AttachedEditWindow","ITextInputPanel::get_AttachedEditWindow","ITextInputPanel::put_AttachedEditWindow","get_AttachedEditWindow","peninputpanel/ITextInputPanel::AttachedEditWindow","peninputpanel/ITextInputPanel::get_AttachedEditWindow","peninputpanel/ITextInputPanel::put_AttachedEditWindow","tablet.itextinputpanel_attachededitwindow"]
old-location: tablet\itextinputpanel_attachededitwindow.htm
tech.root: tablet
ms.assetid: 92a8510d-c8f2-44b4-8812-789ddbc0e3fd
ms.date: 12/05/2018
ms.keywords: 92a8510d-c8f2-44b4-8812-789ddbc0e3fd, AttachedEditWindow property [Tablet PC], AttachedEditWindow property [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],AttachedEditWindow property, ITextInputPanel.AttachedEditWindow, ITextInputPanel.get_AttachedEditWindow, ITextInputPanel.put_AttachedEditWindow, ITextInputPanel::AttachedEditWindow, ITextInputPanel::get_AttachedEditWindow, ITextInputPanel::put_AttachedEditWindow, get_AttachedEditWindow, peninputpanel/ITextInputPanel::AttachedEditWindow, peninputpanel/ITextInputPanel::get_AttachedEditWindow, peninputpanel/ITextInputPanel::put_AttachedEditWindow, tablet.itextinputpanel_attachededitwindow
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
 - ITextInputPanel::get_AttachedEditWindow
 - peninputpanel/ITextInputPanel::get_AttachedEditWindow
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
 - ITextInputPanel.AttachedEditWindow
 - ITextInputPanel.get_AttachedEditWindow
 - ITextInputPanel.put_AttachedEditWindow
 - ITextInputPanel.get_AttachedEditWindow
 - ITextInputPanel.put_AttachedEditWindow
---

# ITextInputPanel::get_AttachedEditWindow


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Gets or sets the window handle of the object to which the <a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> object is attached.



This property is read/write.

## -parameters

## -remarks

The window handle of an object may change.


#### Examples

This C++ example creates an <a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> object, <code>g_pTip</code>, and attaches it to the window handle of an <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control, IDC_EDIT3, by setting the <b>ITextInputPanel::AttachedEditWindow Property</b> property.




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
