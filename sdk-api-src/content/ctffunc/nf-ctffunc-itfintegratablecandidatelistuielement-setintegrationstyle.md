---
UID: NF:ctffunc.ITfIntegratableCandidateListUIElement.SetIntegrationStyle
title: ITfIntegratableCandidateListUIElement::SetIntegrationStyle (ctffunc.h)

description: Sets the integration style.
old-location: tsf\itfintegratablecandidatelistuielement_setintegrationstyle.htm
tech.root: TSF
ms.assetid: DC6565A6-6CEC-4DD9-A845-1DDFF157266C

ms.date: 12/05/2018
ms.keywords: ITfIntegratableCandidateListUIElement interface [Text Services Framework],SetIntegrationStyle method, ITfIntegratableCandidateListUIElement.SetIntegrationStyle, ITfIntegratableCandidateListUIElement::SetIntegrationStyle, SetIntegrationStyle, SetIntegrationStyle method [Text Services Framework], SetIntegrationStyle method [Text Services Framework],ITfIntegratableCandidateListUIElement interface, ctffunc/ITfIntegratableCandidateListUIElement::SetIntegrationStyle, tsf.itfintegratablecandidatelistuielement_setintegrationstyle
ms.topic: method
f1_keywords: 
 - "ctffunc/ITfIntegratableCandidateListUIElement.SetIntegrationStyle"
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
 - ITfIntegratableCandidateListUIElement.SetIntegrationStyle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITfIntegratableCandidateListUIElement::SetIntegrationStyle


## -description


Sets the integration style.


## -parameters




### -param guidIntegrationStyle [in]

The desired type of keyboard integration experience.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The text service supports the integration style.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The text service does not support the integration style.

</td>
</tr>
</table>
 




## -remarks



If an app needs a keyboard-integrated experience, it can set a <b>GUID</b> for the desired type of 
    integration experience.  If the text service supports the integration style, it should return <b>S_OK</b>.
          If it's not supported, it should return <b>E_NOTIMPL</b>.  When called, the text service may adjust its respond to
    keyboard interaction for the lifetime of the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcandidatelistuielement">ITfCandidateListUIElement</a> object, for example, until <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfuielementsink-enduielement">ITfUIElementSink::EndUIElement</a> is called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nn-ctffunc-itfintegratablecandidatelistuielement">ITfIntegratableCandidateListUIElement</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfuielementsink-enduielement">ITfUIElementSink::EndUIElement</a>
 

 

