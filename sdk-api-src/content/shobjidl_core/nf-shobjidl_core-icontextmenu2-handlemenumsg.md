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

# IContextMenu2::HandleMenuMsg


## -description


Enables client objects of the <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> interface to handle messages associated with owner-drawn menu items.


## -parameters




### -param uMsg

Type: <b>UINT</b>

The message to be processed. In the case of some messages, such as WM_INITMENUPOPUP, WM_DRAWITEM, WM_MENUCHAR, or WM_MEASUREITEM, the client object being called may provide owner-drawn menu items.


### -param wParam

Type: <b>WPARAM</b>

Additional message information. The value of this parameter depends on the value of the <i>uMsg</i> parameter.


### -param lParam

Type: <b>LPARAM</b>

Additional message information. The value of this parameter depends on the value of the <i>uMsg</i> parameter.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IContextMenu2::HandleMenuMsg</b> is generally replaced by <a href="https://msdn.microsoft.com/d258edb1-9489-4cdf-b398-16af37a1cb38">HandleMenuMsg2</a>. <b>HandleMenuMsg2</b> is called when <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> determines that <a href="https://msdn.microsoft.com/c08e1b98-2b8b-41f6-93c5-3a5937bd3b2c">IContextMenu3</a> is supported and receives one of the messages specified in the description of the <i>uMsg</i> parameter. However, in some cases, <b>IContextMenu2::HandleMenuMsg</b> is still called.

If <a href="https://msdn.microsoft.com/4e3331ad-4adc-4ea9-8a22-6aad15f618c8">IContextMenu2</a> or <a href="https://msdn.microsoft.com/c08e1b98-2b8b-41f6-93c5-3a5937bd3b2c">IContextMenu3</a> is needed, the best implementation for new context menus is to implement all their logic in <a href="https://msdn.microsoft.com/d258edb1-9489-4cdf-b398-16af37a1cb38">HandleMenuMsg2</a> and have their <b>IContextMenu2::HandleMenuMsg</b> implementation simply delegate the call to <b>HandleMenuMsg2</b> and pass <b>NULL</b> as the <i>plResult</i> parameter.


<div class="alert"><b>Note</b>  
        If <a href="https://msdn.microsoft.com/c08e1b98-2b8b-41f6-93c5-3a5937bd3b2c">IContextMenu3</a> is not implemented, there is no guarantee that <a href="https://msdn.microsoft.com/4e3331ad-4adc-4ea9-8a22-6aad15f618c8">IContextMenu2</a> will be called in its place. In some cases, the absence of <b>IContextMenu3</b> is determined and then the process is halted.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d258edb1-9489-4cdf-b398-16af37a1cb38">HandleMenuMsg2</a>



<a href="https://msdn.microsoft.com/4e3331ad-4adc-4ea9-8a22-6aad15f618c8">IContextMenu2</a>
 

 

