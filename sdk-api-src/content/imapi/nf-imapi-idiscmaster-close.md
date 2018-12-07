---
UID: NF:imapi.IDiscMaster.Close
title: IDiscMaster::Close
author: windows-sdk-content
description: Closes the interface so other applications can use it.
old-location: imapi\idiscmaster_close.htm
tech.root: imapi
ms.assetid: c5ebeca1-baaa-49ac-87ac-134d4b37e8c9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Close, Close method [IMAPI], Close method [IMAPI],IDiscMaster interface, IDiscMaster interface [IMAPI],Close method, IDiscMaster.Close, IDiscMaster::Close, _win32_idiscmaster_close, base.idiscmaster_close, imapi.idiscmaster_close, imapi/IDiscMaster::Close
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscMaster.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscMaster::Close


## -description


Closes the interface so other applications can use it.


## -parameters






## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



Content not committed to media through a call to 
<a href="https://msdn.microsoft.com/2b234dc5-2409-49d8-83be-0ffea74f5bcf">RecordDisc</a> is lost.

Closing an already closed interface returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/1473e79e-a13a-4bc5-b80d-d8921fdc9952">IDiscMaster</a>
 

 

