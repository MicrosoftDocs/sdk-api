---
UID: NF:ctffunc.ITfIntegratableCandidateListUIElement.SetIntegrationStyle
title: ITfIntegratableCandidateListUIElement::SetIntegrationStyle
author: windows-sdk-content
description: Sets the integration style.
old-location: tsf\itfintegratablecandidatelistuielement_setintegrationstyle.htm
old-project: TSF
ms.assetid: DC6565A6-6CEC-4DD9-A845-1DDFF157266C
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: ITfIntegratableCandidateListUIElement interface [Text Services Framework],SetIntegrationStyle method, ITfIntegratableCandidateListUIElement.SetIntegrationStyle, ITfIntegratableCandidateListUIElement::SetIntegrationStyle, SetIntegrationStyle, SetIntegrationStyle method [Text Services Framework], SetIntegrationStyle method [Text Services Framework],ITfIntegratableCandidateListUIElement interface, ctffunc/ITfIntegratableCandidateListUIElement::SetIntegrationStyle, tsf.itfintegratablecandidatelistuielement_setintegrationstyle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ctffunc.h
api_name:
-	ITfIntegratableCandidateListUIElement.SetIntegrationStyle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
    keyboard interaction for the lifetime of the <a href="https://msdn.microsoft.com/1f39aa06-3c94-4959-b857-ca61498d5b5c">ITfCandidateListUIElement</a> object, for example, until <a href="https://msdn.microsoft.com/b29539fe-a240-498b-8267-be243d437005">ITfUIElementSink::EndUIElement</a> is called.




## -see-also




<a href="https://msdn.microsoft.com/F9AB2037-6806-42FC-BD41-F6B6BA047908">ITfIntegratableCandidateListUIElement</a>



<a href="https://msdn.microsoft.com/b29539fe-a240-498b-8267-be243d437005">ITfUIElementSink::EndUIElement</a>
 

 

