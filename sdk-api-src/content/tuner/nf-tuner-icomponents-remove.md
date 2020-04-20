---
UID: NF:tuner.IComponents.Remove
title: IComponents::Remove (tuner.h)
description: The Remove method removes a Component object from the collection.helpviewer_keywords: ["IComponents interface [Microsoft TV Technologies]","Remove method","IComponents.Remove","IComponents::Remove","IComponentsRemove","Remove","Remove method [Microsoft TV Technologies]","Remove method [Microsoft TV Technologies]","IComponents interface","mstv.icomponents_remove","tuner/IComponents::Remove"]
old-location: mstv\icomponents_remove.htm
tech.root: mstv
ms.assetid: 0d71b1f0-1a15-4206-b22f-624cc4b246a3
ms.date: 12/05/2018
ms.keywords: IComponents interface [Microsoft TV Technologies],Remove method, IComponents.Remove, IComponents::Remove, IComponentsRemove, Remove, Remove method [Microsoft TV Technologies], Remove method [Microsoft TV Technologies],IComponents interface, mstv.icomponents_remove, tuner/IComponents::Remove
f1_keywords:
- tuner/IComponents.Remove
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
- IComponents.Remove
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponents::Remove


## -description



The <b>Remove</b> method removes a <b>Component</b> object from the collection.




## -parameters




### -param Index [in]

Variable of type <b>VARIANT</b> that specifies the index number of the <b>Component</b> object to be removed.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponents">IComponents Interface</a>
 

 

