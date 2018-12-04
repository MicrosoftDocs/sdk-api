---
UID: NF:peninputpanel.ITextInputPanel.get_ExpandPostInsertionCorrection
title: ITextInputPanel::get_ExpandPostInsertionCorrection
author: windows-sdk-content
description: Gets or sets a value that indicates whether the correction comb on the Tablet PC Input Panel is automatically expanded.
old-location: tablet\itextinputpanel_expandpostinsertioncorrection.htm
tech.root: tablet
ms.assetid: fda9ac46-7aa0-4991-94df-d71772b90726
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ExpandPostInsertionCorrection property [Tablet PC], ExpandPostInsertionCorrection property [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],ExpandPostInsertionCorrection property, ITextInputPanel.ExpandPostInsertionCorrection, ITextInputPanel.get_ExpandPostInsertionCorrection, ITextInputPanel.put_ExpandPostInsertionCorrection, ITextInputPanel::ExpandPostInsertionCorrection, ITextInputPanel::get_ExpandPostInsertionCorrection, ITextInputPanel::put_ExpandPostInsertionCorrection, fda9ac46-7aa0-4991-94df-d71772b90726, get_ExpandPostInsertionCorrection, peninputpanel/ITextInputPanel::ExpandPostInsertionCorrection, peninputpanel/ITextInputPanel::get_ExpandPostInsertionCorrection, peninputpanel/ITextInputPanel::put_ExpandPostInsertionCorrection, tablet.itextinputpanel_expandpostinsertioncorrection
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
 - ITextInputPanel.ExpandPostInsertionCorrection
 - ITextInputPanel.get_ExpandPostInsertionCorrection
 - ITextInputPanel.put_ExpandPostInsertionCorrection
 - ITextInputPanel.get_ExpandPostInsertionCorrection
 - ITextInputPanel.put_ExpandPostInsertionCorrection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextInputPanel::get_ExpandPostInsertionCorrection


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>.

]


Gets or sets a value that indicates whether the correction comb on the Tablet PC Input Panel is automatically expanded.



This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  In Windows 7, the behavior of the <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> interface has changed. The <i>Expand</i> parameter will always be set to "not expanded" when returned. Setting this property no longer performs any operations.</div>
<div> </div>

#### Examples

This C++ example creates an <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel</a> object, <code>g_pTip</code>, and attaches it to the window handle of an <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control, <code>IDC_EDIT3</code>, by setting the <a href="https://msdn.microsoft.com/92a8510d-c8f2-44b4-8812-789ddbc0e3fd">ITextInputPanel::AttachedEditWindow Property</a> property. It also sets, then gets the <b>ITextInputPanel::ExpandPostInsertionCorrection Property</b>.





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
 

 

