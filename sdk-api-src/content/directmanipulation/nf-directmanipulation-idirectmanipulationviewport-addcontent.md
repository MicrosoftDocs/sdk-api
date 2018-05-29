---
UID: NF:directmanipulation.IDirectManipulationViewport.AddContent
title: IDirectManipulationViewport::AddContent
author: windows-sdk-content
description: Adds secondary content, such as a panning indicator, to a viewport.
old-location: directmanipulation\idirectmanipulationviewport_addcontent.htm
old-project: directmanipulation
ms.assetid: 1c404e9a-832d-47af-b162-2783faa05237
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: AddContent, AddContent method [Direct Manipulation], AddContent method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],AddContent method, IDirectManipulationViewport.AddContent, IDirectManipulationViewport::AddContent, directmanipulation.idirectmanipulationviewport_addcontent, directmanipulation/IDirectManipulationViewport::AddContent
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
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DirectManipulation.h
api_name:
-	IDirectManipulationViewport.AddContent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationViewport::AddContent


## -description


Adds secondary content, such as a panning indicator, to a viewport.


## -parameters




### -param content [in]

The content to add to the viewport.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Secondary content is created by calling <a href="https://msdn.microsoft.com/f8a2fbb2-f662-4eb7-88fb-64286205f19e">CreateContent</a>. Once added, the secondary content will move relative to the primary content in response to a manipulation. Its motion is determined by rules associated with each type of secondary content.




## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

