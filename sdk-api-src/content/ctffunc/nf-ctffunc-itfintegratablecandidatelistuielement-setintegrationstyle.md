---
UID: NF:ctffunc.ITfIntegratableCandidateListUIElement.SetIntegrationStyle
title: ITfIntegratableCandidateListUIElement::SetIntegrationStyle
author: windows-sdk-content
description: Sets the integration style.
old-location: tsf\itfintegratablecandidatelistuielement_setintegrationstyle.htm
tech.root: TSF
ms.assetid: DC6565A6-6CEC-4DD9-A845-1DDFF157266C
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITfIntegratableCandidateListUIElement interface [Text Services Framework],SetIntegrationStyle method, ITfIntegratableCandidateListUIElement.SetIntegrationStyle, ITfIntegratableCandidateListUIElement::SetIntegrationStyle, SetIntegrationStyle, SetIntegrationStyle method [Text Services Framework], SetIntegrationStyle method [Text Services Framework],ITfIntegratableCandidateListUIElement interface, ctffunc/ITfIntegratableCandidateListUIElement::SetIntegrationStyle, tsf.itfintegratablecandidatelistuielement_setintegrationstyle
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
    keyboard interaction for the lifetime of the <a href="https://msdn.microsoft.com/en-us/library/Aa380892(v=VS.85).aspx">ITfCandidateListUIElement</a> object, for example, until <a href="https://msdn.microsoft.com/en-us/library/Aa383204(v=VS.85).aspx">ITfUIElementSink::EndUIElement</a> is called.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh920954(v=VS.85).aspx">ITfIntegratableCandidateListUIElement</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383204(v=VS.85).aspx">ITfUIElementSink::EndUIElement</a>
 

 

