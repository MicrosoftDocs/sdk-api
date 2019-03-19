---
UID: NF:tuner.IComponent.put_Type
title: IComponent::put_Type (tuner.h)
author: windows-sdk-content
description: The put_Type method sets an IComponentType object describing the general characteristics of the component.
old-location: mstv\icomponent_put_type.htm
tech.root: mstv
ms.assetid: 07d8cc28-d34e-4332-8648-d69a471ca8ac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],put_Type method, IComponent.put_Type, IComponent::put_Type, IComponentput_Type, mstv.icomponent_put_type, put_Type, put_Type method [Microsoft TV Technologies], put_Type method [Microsoft TV Technologies],IComponent interface, tuner/IComponent::put_Type
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
 - IComponent.put_Type
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComponent::put_Type


## -description



The <b>put_Type</b> method sets an <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a> object describing the general characteristics of the component.




## -parameters




### -param CT [in]

Pointer to an <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a> object that specifies the new values for the component.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



Using the <a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent</a> base class interface, it is possible to set the type to be <b>NULL</b>. If you try to do this with the derived <a href="https://msdn.microsoft.com/63d1ae17-8e38-457e-98d7-e81e7576f1c1">IMPEG2Component</a> class interface, this method will return E_POINTER. The <b>IMPEG2Component</b> object cannot have the base <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a> class interface as the set type - this will return Type Mismatch (0x80020005).




## -see-also




<a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent Interface</a>
 

 

