---
UID: NN:ctffunc.ITfIntegratableCandidateListUIElement
title: ITfIntegratableCandidateListUIElement (ctffunc.h)

description: Enables text services and Input Method Editors (IMEs) to adjust UI-less mode behavior.
old-location: tsf\itfintegratablecandidatelistuielement.htm
tech.root: TSF
ms.assetid: F9AB2037-6806-42FC-BD41-F6B6BA047908

ms.date: 12/05/2018
ms.keywords: ITfIntegratableCandidateListUIElement, ITfIntegratableCandidateListUIElement interface [Text Services Framework], ITfIntegratableCandidateListUIElement interface [Text Services Framework],described, ctffunc/ITfIntegratableCandidateListUIElement, tsf.itfintegratablecandidatelistuielement
ms.topic: interface
f1_keywords: 
 - "ctffunc/ITfIntegratableCandidateListUIElement"
dev_langs:
 - c++
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ctffunc.h
api_name:
 - ITfIntegratableCandidateListUIElement
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITfIntegratableCandidateListUIElement interface


## -description


Enables text services and Input Method Editors (IMEs) to adjust UI-less mode behavior. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfIntegratableCandidateListUIElement</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfIntegratableCandidateListUIElement</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfIntegratableCandidateListUIElement</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itfintegratablecandidatelistuielement-finalizeexactcompositionstring">FinalizeExactCompositionString</a>
</td>
<td align="left" width="63%">
Finalizes the current composition with the value currently shown to the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itfintegratablecandidatelistuielement-getselectionstyle">GetSelectionStyle</a>
</td>
<td align="left" width="63%">
Retrieves the selection style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itfintegratablecandidatelistuielement-onkeydown">OnKeyDown</a>
</td>
<td align="left" width="63%">
Processes a key press.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itfintegratablecandidatelistuielement-setintegrationstyle">SetIntegrationStyle</a>
</td>
<td align="left" width="63%">
Sets the integration style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-itfintegratablecandidatelistuielement-showcandidatenumbers">ShowCandidateNumbers</a>
</td>
<td align="left" width="63%">
Specifies whether candidate numbers should be shown.

</td>
</tr>
</table> 


## -remarks



The <b>ITfIntegratableCandidateListUIElement</b> interface is implemented by text services and Input Method Editors (IMEs) to adjust UI-less mode behavior for a better UI and keyboarding experience in IME-integrated controls, like the Windows 8 Search box.  The interface is used by apps that need a more streamlined UI and keyboarding experience with IME languages. 

You can get an <b>ITfIntegratableCandidateListUIElement</b> interface pointer by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfuielement">ITfUIElement</a> interface pointer that's provided by using the <i>dwUIElementId</i> parameters of the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfuielementsink">ITfUIElementSink</a> callback functions to obtain the interface from  <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfuielementmgr">ITfUIElementMgr</a>.

The <b>ITfIntegratableCandidateListUIElement</b> interface is an optional interface that's implemented by a text service or IME that needs greater control over how its UI is presented in UI-less mode.  Apps can use it to implement more streamlined, special-purpose input controls, as in auto-complete or search suggestions.

Implement the <b>ITfIntegratableCandidateListUIElement</b> interface in the same class that implements the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfuielement">ITfUIElement</a>, <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcandidatelistuielement">ITfCandidateListUIElement</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcandidatelistuielementbehavior">ITfCandidateListUIElementBehavior</a> interfaces.  These interfaces work together to create a fully integrated experience in which the app renders candidate list UI for the text service or IME and can also have some IME-specific UI customization and keyboard interaction behavior.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcandidatelistuielement">ITfCandidateListUIElement</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcandidatelistuielementbehavior">ITfCandidateListUIElementBehavior</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfuielement">ITfUIElement</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfuielementmgr">ITfUIElementMgr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfuielementsink">ITfUIElementSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

