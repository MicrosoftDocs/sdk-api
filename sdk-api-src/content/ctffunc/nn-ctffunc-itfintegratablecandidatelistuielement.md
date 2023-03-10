---
UID: NN:ctffunc.ITfIntegratableCandidateListUIElement
title: ITfIntegratableCandidateListUIElement (ctffunc.h)
description: Enables text services and Input Method Editors (IMEs) to adjust UI-less mode behavior.
helpviewer_keywords: ["ITfIntegratableCandidateListUIElement","ITfIntegratableCandidateListUIElement interface [Text Services Framework]","ITfIntegratableCandidateListUIElement interface [Text Services Framework]","described","ctffunc/ITfIntegratableCandidateListUIElement","tsf.itfintegratablecandidatelistuielement"]
old-location: tsf\itfintegratablecandidatelistuielement.htm
tech.root: TSF
ms.assetid: F9AB2037-6806-42FC-BD41-F6B6BA047908
ms.date: 12/05/2018
ms.keywords: ITfIntegratableCandidateListUIElement, ITfIntegratableCandidateListUIElement interface [Text Services Framework], ITfIntegratableCandidateListUIElement interface [Text Services Framework],described, ctffunc/ITfIntegratableCandidateListUIElement, tsf.itfintegratablecandidatelistuielement
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfIntegratableCandidateListUIElement
 - ctffunc/ITfIntegratableCandidateListUIElement
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ctffunc.h
api_name:
 - ITfIntegratableCandidateListUIElement
---

# ITfIntegratableCandidateListUIElement interface


## -description

Enables text services and Input Method Editors (IMEs) to adjust UI-less mode behavior.

## -inheritance

The <b>ITfIntegratableCandidateListUIElement</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfIntegratableCandidateListUIElement</b> also has these types of members:

## -remarks

The <b>ITfIntegratableCandidateListUIElement</b> interface is implemented by text services and Input Method Editors (IMEs) to adjust UI-less mode behavior for a better UI and keyboarding experience in IME-integrated controls, like the Windows 8 Search box.  The interface is used by apps that need a more streamlined UI and keyboarding experience with IME languages. 

You can get an <b>ITfIntegratableCandidateListUIElement</b> interface pointer by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the <a href="/windows/desktop/api/msctf/nn-msctf-itfuielement">ITfUIElement</a> interface pointer that's provided by using the <i>dwUIElementId</i> parameters of the <a href="/windows/desktop/api/msctf/nn-msctf-itfuielementsink">ITfUIElementSink</a> callback functions to obtain the interface from  <a href="/windows/desktop/api/msctf/nn-msctf-itfuielementmgr">ITfUIElementMgr</a>.

The <b>ITfIntegratableCandidateListUIElement</b> interface is an optional interface that's implemented by a text service or IME that needs greater control over how its UI is presented in UI-less mode.  Apps can use it to implement more streamlined, special-purpose input controls, as in auto-complete or search suggestions.

Implement the <b>ITfIntegratableCandidateListUIElement</b> interface in the same class that implements the <a href="/windows/desktop/api/msctf/nn-msctf-itfuielement">ITfUIElement</a>, <a href="/windows/desktop/api/msctf/nn-msctf-itfcandidatelistuielement">ITfCandidateListUIElement</a>, and <a href="/windows/desktop/api/msctf/nn-msctf-itfcandidatelistuielementbehavior">ITfCandidateListUIElementBehavior</a> interfaces.  These interfaces work together to create a fully integrated experience in which the app renders candidate list UI for the text service or IME and can also have some IME-specific UI customization and keyboard interaction behavior.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcandidatelistuielement">ITfCandidateListUIElement</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcandidatelistuielementbehavior">ITfCandidateListUIElementBehavior</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfuielement">ITfUIElement</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfuielementmgr">ITfUIElementMgr</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfuielementsink">ITfUIElementSink</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
