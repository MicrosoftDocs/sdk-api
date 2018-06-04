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

# IDiscMaster::SetActiveDiscMasterFormat


## -description


Sets the currently active disc recorder format. The active format specifies both the structure of the staged image file content (audio/data) and the COM interface that must be used to manipulate that staged image.


## -parameters




### -param riid [in]

IID of the currently active format.


### -param ppUnk [out]

Pointer to the COM interface for the new disc format.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



A successful call to this method clears the contents of the currently staged image. In addition, it may change the list of supported disc recorders. This is because not all recorders support all formats. Changes to the recorder list are announced with 
<a href="https://msdn.microsoft.com/d2b41e86-2f1b-46f1-955d-7fc42f8189a4">IDiscMasterProgressEvents::NotifyPnPActivity</a>. If the currently selected recorder is not a member of the new set of supported devices, then there will no longer be an active recorder (similar to the state after the first call to 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>). In this case, the application must select a new active recorder before initiating a burn.

<b>MSDiscMasterObj</b> supports only the following IIDs: IID_IRedbookDiscMaster (<a href="https://msdn.microsoft.com/ea531b22-869a-400e-801f-00bb85ebaac2">IRedbookDiscMaster</a>) and IID_IJolietDiscMaster (<a href="https://msdn.microsoft.com/e2269b68-1860-4afd-90f2-d61297f3fa9b">IJolietDiscMaster</a>). If there is no format set, the default is Joliet format. It is the responsibility of every application to select a format master through the use of 
<a href="https://msdn.microsoft.com/7190dbf6-6458-4228-a892-428183ea2742">EnumDiscMasterFormats</a> and this method.

<div class="alert"><b>Note</b>  A call to this method may change the list of available recorders. See the Remarks section of 
<a href="https://msdn.microsoft.com/03daab81-11cf-4100-ab5e-3442a5972912">EnumDiscRecorders</a> for more information.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/1473e79e-a13a-4bc5-b80d-d8921fdc9952">IDiscMaster</a>
 

 

