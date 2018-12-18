---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.SetSnapType
title: IDirectManipulationPrimaryContent::SetSnapType
author: windows-sdk-content
description: Specifies the type of snap point.
old-location: directmanipulation\idirectmanipulationprimarycontent_setsnaptype.htm
tech.root: directmanipulation
ms.assetid: 0f1ad54d-8c9a-4b3c-a78b-fe02cb889ca9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectManipulationPrimaryContent interface [Direct Manipulation],SetSnapType method, IDirectManipulationPrimaryContent.SetSnapType, IDirectManipulationPrimaryContent::SetSnapType, SetSnapType, SetSnapType method [Direct Manipulation], SetSnapType method [Direct Manipulation],IDirectManipulationPrimaryContent interface, directmanipulation.idirectmanipulationprimarycontent_setsnaptype, directmanipulation/IDirectManipulationPrimaryContent::SetSnapType
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
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
 - DirectManipulation.h
api_name:
 - IDirectManipulationPrimaryContent.SetSnapType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationPrimaryContent::SetSnapType


## -description


Specifies the type of snap point.


## -parameters




### -param motion [in]

One or more of the <a href="https://msdn.microsoft.com/a0b4da55-3ebb-4281-a372-4bc6b91e6789">DIRECTMANIPULATION_MOTION_TYPES</a> enumeration values.


### -param type [in]

One of the <a href="https://msdn.microsoft.com/4ba8c216-a5bb-409d-bce8-fc85023b63d9">DIRECTMANIPULATION_SNAPPOINT_TYPE</a> enumeration values.

If set to <b>DIRECTMANIPULATION_SNAPPOINT_TYPE_NONE</b>, snap points specified through <a href="https://msdn.microsoft.com/3257952d-903b-455c-9422-9739411a5924">SetSnapPoints</a> or <a href="https://msdn.microsoft.com/99d039fe-017a-47c5-95a1-5000efe92ba0">SetSnapInterval</a> are cleared.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9910F5F5-950F-4099-9808-B46FA5BBA6FB">IDirectManipulationPrimaryContent</a>
 

 

