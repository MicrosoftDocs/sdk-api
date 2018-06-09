---
UID: NF:tuner.IComponent.put_DescLangID
title: IComponent::put_DescLangID
author: windows-sdk-content
description: The put_DescLangID method sets the language for presentation of the description.
old-location: mstv\icomponent_put_desclangid.htm
old-project: mstv
ms.assetid: 0f914835-e097-4a02-80fe-371154c9d95a
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],put_DescLangID method, IComponent.put_DescLangID, IComponent::put_DescLangID, IComponentput_DescLangID, mstv.icomponent_put_desclangid, put_DescLangID, put_DescLangID method [Microsoft TV Technologies], put_DescLangID method [Microsoft TV Technologies],IComponent interface, tuner/IComponent::put_DescLangID
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IComponent.put_DescLangID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponent::put_DescLangID


## -description



The <b>put_DescLangID</b> method sets the language for presentation of the description.




## -parameters




### -param LangID [in]

Specifies the language ID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This is the language of the descriptive info in the component object. It is not the same as the language ID in the language component type which defines the language of the stream content. An application can modify this value in order to activate a different language substream.




## -see-also




<a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent Interface</a>
 

 

