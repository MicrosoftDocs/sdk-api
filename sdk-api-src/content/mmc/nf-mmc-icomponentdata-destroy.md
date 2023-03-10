---
UID: NF:mmc.IComponentData.Destroy
title: IComponentData::Destroy (mmc.h)
description: The IComponentData::Destroy method releases all references to the console.
helpviewer_keywords: ["Destroy","Destroy method [MMC]","Destroy method [MMC]","IComponentData interface","IComponentData interface [MMC]","Destroy method","IComponentData.Destroy","IComponentData::Destroy","_slate_icomponentdata_destroy","mmc.icomponentdata_destroy","mmc/IComponentData::Destroy"]
old-location: mmc\icomponentdata_destroy.htm
tech.root: mmc
ms.assetid: adf7238d-b452-499b-8924-2ea1bfecd69f
ms.date: 12/05/2018
ms.keywords: Destroy, Destroy method [MMC], Destroy method [MMC],IComponentData interface, IComponentData interface [MMC],Destroy method, IComponentData.Destroy, IComponentData::Destroy, _slate_icomponentdata_destroy, mmc.icomponentdata_destroy, mmc/IComponentData::Destroy
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComponentData::Destroy
 - mmc/IComponentData::Destroy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IComponentData.Destroy
---

# IComponentData::Destroy


## -description

The <b>IComponentData::Destroy</b> method releases all references to the console.



## -returns

This method can return one of these values.

## -remarks

The snap-in is in the process of being unloaded. Release all references to the console.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Only the console calls this method.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>



<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-destroy">IComponent::Destroy</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>
