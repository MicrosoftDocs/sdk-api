---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.GetCenterPoint
title: IDirectManipulationPrimaryContent::GetCenterPoint
author: windows-sdk-content
description: Retrieves the center point of the manipulation in content coordinates.
old-location: directmanipulation\idirectmanipulationprimarycontent_getcenterpoint.htm
old-project: directmanipulation
ms.assetid: e38c1445-af4b-463b-8796-d72d69cb19c6
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetCenterPoint, GetCenterPoint method [Direct Manipulation], GetCenterPoint method [Direct Manipulation],IDirectManipulationPrimaryContent interface, IDirectManipulationPrimaryContent interface [Direct Manipulation],GetCenterPoint method, IDirectManipulationPrimaryContent.GetCenterPoint, IDirectManipulationPrimaryContent::GetCenterPoint, directmanipulation.idirectmanipulationprimarycontent_getcenterpoint, directmanipulation/IDirectManipulationPrimaryContent::GetCenterPoint
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DirectManipulation.h
api_name:
-	IDirectManipulationPrimaryContent.GetCenterPoint
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationPrimaryContent::GetCenterPoint


## -description


    Retrieves the center point of the manipulation in content coordinates. If there is no manipulation in progress, retrieves the center point of the viewport.


## -parameters




### -param centerX [out]

The center on the horizontal axis.


### -param centerY [out]

The center on the vertical axis.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9910F5F5-950F-4099-9808-B46FA5BBA6FB">IDirectManipulationPrimaryContent</a>
 

 

