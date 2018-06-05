---
UID: NF:tuner.IComponent.get_Status
title: IComponent::get_Status
author: windows-sdk-content
description: The get_Status method retrieves the requested or actual status of the component.
old-location: mstv\icomponent_get_status.htm
old-project: mstv
ms.assetid: 3f517db8-a207-472e-8c6c-7cb2cac91f62
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],get_Status method, IComponent.get_Status, IComponent::get_Status, IComponentget_Status, get_Status, get_Status method [Microsoft TV Technologies], get_Status method [Microsoft TV Technologies],IComponent interface, mstv.icomponent_get_status, tuner/IComponent::get_Status
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IComponent.get_Status
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponent::get_Status


## -description



The <b>get_Status</b> method retrieves the requested or actual status of the component.




## -parameters




### -param Status






#### - pStatus [out]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff557723">ComponentStatus</a> enumeration that receives the status value.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



When the TIF adds a component to the <a href="https://msdn.microsoft.com/670b47ba-bcbd-4281-95e3-a5d784f0610b">IComponents</a> collection, it can indicate whether the component is active or not. An application can attempt to set this status, and resubmit a tune request. The tuner will update the status from the enumeration: Active, Inactive, Unavailable. The Unavailable status is only set by a tuner in response to a request to activate, when the component is not really available.




## -see-also




<a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent Interface</a>
 

 

