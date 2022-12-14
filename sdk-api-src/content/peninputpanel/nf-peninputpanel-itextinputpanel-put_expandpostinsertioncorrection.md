---
UID: NF:peninputpanel.ITextInputPanel.put_ExpandPostInsertionCorrection
title: ITextInputPanel::put_ExpandPostInsertionCorrection (peninputpanel.h)
description: Gets or sets a value that indicates whether the correction comb on the Tablet PC Input Panel is automatically expanded. (Put)
helpviewer_keywords: ["ExpandPostInsertionCorrection property [Tablet PC]","ExpandPostInsertionCorrection property [Tablet PC]","ITextInputPanel interface","ITextInputPanel interface [Tablet PC]","ExpandPostInsertionCorrection property","ITextInputPanel.ExpandPostInsertionCorrection","ITextInputPanel.get_ExpandPostInsertionCorrection","ITextInputPanel.put_ExpandPostInsertionCorrection","ITextInputPanel::ExpandPostInsertionCorrection","ITextInputPanel::get_ExpandPostInsertionCorrection","ITextInputPanel::put_ExpandPostInsertionCorrection","fda9ac46-7aa0-4991-94df-d71772b90726","peninputpanel/ITextInputPanel::ExpandPostInsertionCorrection","peninputpanel/ITextInputPanel::get_ExpandPostInsertionCorrection","peninputpanel/ITextInputPanel::put_ExpandPostInsertionCorrection","put_ExpandPostInsertionCorrection","tablet.itextinputpanel_expandpostinsertioncorrection"]
old-location: tablet\itextinputpanel_expandpostinsertioncorrection.htm
tech.root: tablet
ms.assetid: fda9ac46-7aa0-4991-94df-d71772b90726
ms.date: 12/05/2018
ms.keywords: ExpandPostInsertionCorrection property [Tablet PC], ExpandPostInsertionCorrection property [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],ExpandPostInsertionCorrection property, ITextInputPanel.ExpandPostInsertionCorrection, ITextInputPanel.get_ExpandPostInsertionCorrection, ITextInputPanel.put_ExpandPostInsertionCorrection, ITextInputPanel::ExpandPostInsertionCorrection, ITextInputPanel::get_ExpandPostInsertionCorrection, ITextInputPanel::put_ExpandPostInsertionCorrection, fda9ac46-7aa0-4991-94df-d71772b90726, peninputpanel/ITextInputPanel::ExpandPostInsertionCorrection, peninputpanel/ITextInputPanel::get_ExpandPostInsertionCorrection, peninputpanel/ITextInputPanel::put_ExpandPostInsertionCorrection, put_ExpandPostInsertionCorrection, tablet.itextinputpanel_expandpostinsertioncorrection
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
 - ITextInputPanel::put_ExpandPostInsertionCorrection
 - peninputpanel/ITextInputPanel::put_ExpandPostInsertionCorrection
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
 - ITextInputPanel.ExpandPostInsertionCorrection
 - ITextInputPanel.get_ExpandPostInsertionCorrection
 - ITextInputPanel.put_ExpandPostInsertionCorrection
 - ITextInputPanel.get_ExpandPostInsertionCorrection
 - ITextInputPanel.put_ExpandPostInsertionCorrection
---

# ITextInputPanel::put_ExpandPostInsertionCorrection


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Gets or sets a value that indicates whether the correction comb on the Tablet PC Input Panel is automatically expanded.



This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  In Windows 7, the behavior of the <a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> interface has changed. The <i>Expand</i> parameter will always be set to "not expanded" when returned. Setting this property no longer performs any operations.</div>
<div> </div>

#### Examples

This C++ example creates an <a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> object, <code>g_pTip</code>, and attaches it to the window handle of an <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control, <code>IDC_EDIT3</code>, by setting the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_attachededitwindow">ITextInputPanel::AttachedEditWindow Property</a> property. It also sets, then gets the <b>ITextInputPanel::ExpandPostInsertionCorrection Property</b>.






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
