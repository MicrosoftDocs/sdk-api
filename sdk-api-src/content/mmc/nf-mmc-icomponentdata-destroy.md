---
UID: NF:mmc.IComponentData.Destroy
title: IComponentData::Destroy
author: windows-sdk-content
description: The IComponentData::Destroy method releases all references to the console.
old-location: mmc\icomponentdata_destroy.htm
old-project: mmc
ms.assetid: adf7238d-b452-499b-8924-2ea1bfecd69f
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: Destroy, Destroy method [MMC], Destroy method [MMC],IComponentData interface, IComponentData interface [MMC],Destroy method, IComponentData.Destroy, IComponentData::Destroy, _slate_icomponentdata_destroy, mmc.icomponentdata_destroy, mmc/IComponentData::Destroy
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IComponentData.Destroy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IComponentData::Destroy


## -description


The <b>IComponentData::Destroy</b> method releases all references to the console.


## -parameters






## -returns



This method can return one of these values.




## -remarks



The snap-in is in the process of being unloaded. Release all references to the console.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Only the console calls this method.




## -see-also




<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>



<a href="https://msdn.microsoft.com/ec4ec242-6376-44e7-bd82-09456789c4c9">IComponent::Destroy</a>



<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>



<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>
 

 

