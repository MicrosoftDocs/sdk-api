---
UID: NF:mmc.IComponent.Destroy
title: IComponent::Destroy
author: windows-sdk-content
description: The IComponent::Destroy method releases all references to the console that are held by this component.
old-location: mmc\icomponent_destroy.htm
tech.root: MMC
ms.assetid: ec4ec242-6376-44e7-bd82-09456789c4c9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Destroy, Destroy method [MMC], Destroy method [MMC],IComponent interface, IComponent interface [MMC],Destroy method, IComponent.Destroy, IComponent::Destroy, _slate_icomponent_destroy, mmc.icomponent_destroy, mmc/IComponent::Destroy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Mmc.h
api_name:
 - IComponent.Destroy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mmc.h
: 
- IComponent.Destroy
: 
---

# IComponent::Destroy


## -description


The IComponent::Destroy method releases all references to the console that are held by this component.


## -parameters




### -param cookie

Reserved for future use.


## -returns



This method can return one of these values.




## -remarks



The snap-in is in the process of being unloaded. It should release all references to the console contained by the component.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Only the console calls this method.




## -see-also




<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>
 

 

