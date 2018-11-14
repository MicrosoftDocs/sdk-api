---
UID: NF:tuner.IComponent.get_DescLangID
title: IComponent::get_DescLangID
author: windows-sdk-content
description: The get_DescLangID method retrieves the language identifier for the description property.
old-location: mstv\icomponent_get_desclangid.htm
tech.root: MSTV
ms.assetid: 1c041173-0c78-486e-93b5-a46c9dc0afb1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],get_DescLangID method, IComponent.get_DescLangID, IComponent::get_DescLangID, IComponentget_DescLangID, get_DescLangID, get_DescLangID method [Microsoft TV Technologies], get_DescLangID method [Microsoft TV Technologies],IComponent interface, mstv.icomponent_get_desclangid, tuner/IComponent::get_DescLangID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IComponent.get_DescLangID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tuner.h
: 
- IComponent.get_DescLangID
: 
---

# IComponent::get_DescLangID


## -description



The <b>get_DescLangID</b> method retrieves the language identifier for the description property.




## -parameters




### -param LangID

TBD




#### - pLangID [out]

Receives the language identifier.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The returned language identifer identifies the language of the description property, which is obtained by calling the <b>get_Description</b> method.

To get the language of the stream content, call the <a href="https://msdn.microsoft.com/f70dcc70-701a-4465-ad40-1ddc5e697f46">ILanguageComponentType::get_LangID</a> method (only if the component object exposes the <a href="https://msdn.microsoft.com/775b5e8d-d9ed-4371-a651-bfeed6fa0ad5">ILanguageComponentType</a> interface).




## -see-also




<a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent Interface</a>



<a href="https://msdn.microsoft.com/ef7d1308-27ff-4d4d-b88d-58a9f89abc7f">IComponent::get_Description</a>
 

 

