---
UID: NN:ctffunc.ITfIntegratableCandidateListUIElement
title: ITfIntegratableCandidateListUIElement
author: windows-sdk-content
description: Enables text services and Input Method Editors (IMEs) to adjust UI-less mode behavior.
old-location: tsf\itfintegratablecandidatelistuielement.htm
tech.root: TSF
ms.assetid: F9AB2037-6806-42FC-BD41-F6B6BA047908
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITfIntegratableCandidateListUIElement, ITfIntegratableCandidateListUIElement interface [Text Services Framework], ITfIntegratableCandidateListUIElement interface [Text Services Framework],described, ctffunc/ITfIntegratableCandidateListUIElement, tsf.itfintegratablecandidatelistuielement
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITfIntegratableCandidateListUIElement interface


## -description


Enables text services and Input Method Editors (IMEs) to adjust UI-less mode behavior. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfIntegratableCandidateListUIElement</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfIntegratableCandidateListUIElement</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1A81C1D7-2D7A-41A0-9DB7-0F30AE610051">FinalizeExactCompositionString</a>
</td>
<td align="left" width="63%">
Finalizes the current composition with the value currently shown to the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D51E27FE-503E-459C-92F1-1826762A5188">GetSelectionStyle</a>
</td>
<td align="left" width="63%">
Retrieves the selection style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EF6A8FB1-9B48-44BE-A1B4-AA3F2EA0F6BA">OnKeyDown</a>
</td>
<td align="left" width="63%">
Processes a key press.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DC6565A6-6CEC-4DD9-A845-1DDFF157266C">SetIntegrationStyle</a>
</td>
<td align="left" width="63%">
Sets the integration style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91F40471-69D0-457B-9614-1B5A690A82B7">ShowCandidateNumbers</a>
</td>
<td align="left" width="63%">
Specifies whether candidate numbers should be shown.

</td>
</tr>
</table> 


## -remarks



The <b>ITfIntegratableCandidateListUIElement</b> interface is implemented by text services and Input Method Editors (IMEs) to adjust UI-less mode behavior for a better UI and keyboarding experience in IME-integrated controls, like the Windows 8 Search box.  The interface is used by apps that need a more streamlined UI and keyboarding experience with IME languages. 

You can get an <b>ITfIntegratableCandidateListUIElement</b> interface pointer by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the <a href="https://msdn.microsoft.com/651c3ca1-5e5b-4978-80d2-2183bd158610">ITfUIElement</a> interface pointer that's provided by using the <i>dwUIElementId</i> parameters of the <a href="https://msdn.microsoft.com/8f77b3bc-2e47-4966-8030-d05a626ee00a">ITfUIElementSink</a> callback functions to obtain the interface from  <a href="https://msdn.microsoft.com/7b4d3f4e-bf30-45c6-8709-88b71b25d333">ITfUIElementMgr</a>.

The <b>ITfIntegratableCandidateListUIElement</b> interface is an optional interface that's implemented by a text service or IME that needs greater control over how its UI is presented in UI-less mode.  Apps can use it to implement more streamlined, special-purpose input controls, as in auto-complete or search suggestions.

Implement the <b>ITfIntegratableCandidateListUIElement</b> interface in the same class that implements the <a href="https://msdn.microsoft.com/651c3ca1-5e5b-4978-80d2-2183bd158610">ITfUIElement</a>, <a href="https://msdn.microsoft.com/1f39aa06-3c94-4959-b857-ca61498d5b5c">ITfCandidateListUIElement</a>, and <a href="https://msdn.microsoft.com/3e1c53c6-f356-4b60-bb85-0f5a7251219d">ITfCandidateListUIElementBehavior</a> interfaces.  These interfaces work together to create a fully integrated experience in which the app renders candidate list UI for the text service or IME and can also have some IME-specific UI customization and keyboard interaction behavior.




## -see-also




<a href="https://msdn.microsoft.com/1f39aa06-3c94-4959-b857-ca61498d5b5c">ITfCandidateListUIElement</a>



<a href="https://msdn.microsoft.com/3e1c53c6-f356-4b60-bb85-0f5a7251219d">ITfCandidateListUIElementBehavior</a>



<a href="https://msdn.microsoft.com/651c3ca1-5e5b-4978-80d2-2183bd158610">ITfUIElement</a>



<a href="https://msdn.microsoft.com/7b4d3f4e-bf30-45c6-8709-88b71b25d333">ITfUIElementMgr</a>



<a href="https://msdn.microsoft.com/8f77b3bc-2e47-4966-8030-d05a626ee00a">ITfUIElementSink</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

