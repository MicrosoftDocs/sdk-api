---
UID: NF:tuner.IEnumComponents.Clone
title: IEnumComponents::Clone (tuner.h)
author: windows-sdk-content
description: The Clone method creates a new copy of the entire collection.
old-location: mstv\ienumcomponents_clone.htm
tech.root: mstv
ms.assetid: ca15a67e-1788-4f57-bfe8-ec1a3014044f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],IEnumComponents interface, IEnumComponents interface [Microsoft TV Technologies],Clone method, IEnumComponents.Clone, IEnumComponents::Clone, IEnumComponentsClone, mstv.ienumcomponents_clone, tuner/IEnumComponents::Clone
ms.topic: method
f1_keywords: 
 - "tuner/IEnumComponents.Clone"
dev_langs:
 - c++
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
 - IEnumComponents.Clone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumComponents::Clone


## -description



The <b>Clone</b> method creates a new copy of the entire collection.




## -parameters




### -param ppEnum [out]

Address of an <b>IEnumComponents</b> interface pointer that will be set to the new collection.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The application must release this new collection when done with it.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ienumcomponents">IEnumComponents Interface</a>
 

 

