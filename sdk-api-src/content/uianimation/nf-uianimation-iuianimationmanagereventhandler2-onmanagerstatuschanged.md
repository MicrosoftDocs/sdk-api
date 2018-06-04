---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUIAnimationManagerEventHandler2::OnManagerStatusChanged


## -description



      Handles status changes to an <a href="https://msdn.microsoft.com/BD7DAD23-2A7D-4EE7-9BCF-8380F928674D">animation manager</a>.


## -parameters




### -param newStatus [in]


               The new status of the animation manager.


### -param previousStatus [in]


               The previous status of the animation manager.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Calls made to other Windows Animation methods from <b>IUIAnimationManager2::OnManagerStatusChanged</b> fail and return <b>UI_E_ILLEGAL_REENTRANCY</b>.




## -see-also




<a href="https://msdn.microsoft.com/E989CED1-C6B7-4086-944E-924836AA7ECB">
      IUIAnimationManager2::GetStatus</a>



<a href="https://msdn.microsoft.com/3D3DAC6C-6904-4962-BB17-18FA97678834">IUIAnimationManagerEventHandler2</a>



<a href="https://msdn.microsoft.com/499c74c0-d1e7-4ab4-9c3a-19c2e1abeda8">
      UI_ANIMATION_MANAGER_STATUS</a>
 

 

