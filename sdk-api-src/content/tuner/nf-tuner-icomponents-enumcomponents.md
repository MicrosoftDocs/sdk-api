---
UID: NF:tuner.IComponents.EnumComponents
title: IComponents::EnumComponents (tuner.h)
author: windows-sdk-content
description: The EnumComponents method returns an enumerator for the components in the collection.
old-location: mstv\icomponents_enumcomponents.htm
tech.root: mstv
ms.assetid: 214030ff-8aec-46df-8b59-f31fe926d8aa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumComponents, EnumComponents method [Microsoft TV Technologies], EnumComponents method [Microsoft TV Technologies],IComponents interface, IComponents interface [Microsoft TV Technologies],EnumComponents method, IComponents.EnumComponents, IComponents::EnumComponents, IComponentsEnumComponents, mstv.icomponents_enumcomponents, tuner/IComponents::EnumComponents
ms.topic: method
f1_keywords: 
 - "tuner/IComponents.EnumComponents"
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
 - IComponents.EnumComponents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponents::EnumComponents


## -description



The <b>EnumComponents</b> method returns an enumerator for the components in the collection.




## -parameters




### -param ppNewEnum [out]

Address of a variable that receives an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumcomponents">IEnumComponents</a> interface pointer.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



If the method succeeds, the <b>IEnumComponents</b> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponents">IComponents Interface</a>
 

 

