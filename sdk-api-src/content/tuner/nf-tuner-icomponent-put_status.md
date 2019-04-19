---
UID: NF:tuner.IComponent.put_Status
title: IComponent::put_Status (tuner.h)
author: windows-sdk-content
description: The put_Status method sets the requested or actual status of the component.
old-location: mstv\icomponent_put_status.htm
tech.root: mstv
ms.assetid: f1f9cf98-69fd-4c54-8023-742f86413220
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],put_Status method, IComponent.put_Status, IComponent::put_Status, IComponentput_Status, mstv.icomponent_put_status, put_Status, put_Status method [Microsoft TV Technologies], put_Status method [Microsoft TV Technologies],IComponent interface, tuner/IComponent::put_Status
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
 - IComponent.put_Status
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponent::put_Status


## -description



The <b>put_Status</b> method sets the requested or actual status of the component.




## -parameters




### -param Status [in]

A variable of type <a href="https://msdn.microsoft.com/687ae778-0c25-47ca-bec9-9e6c28f22249">ComponentStatus</a> that specifies the status value.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



Use this method to activate or inactivate a stream component.




## -see-also




<a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent Interface</a>



<a href="https://msdn.microsoft.com/3f517db8-a207-472e-8c6c-7cb2cac91f62">IComponent::get_Status</a>
 

 

