---
UID: NF:imapi2.IMultisession.put_InUse
title: IMultisession::put_InUse
author: windows-sdk-content
description: Determines if this multi-session interface is the one you should use on the current media.
old-location: imapi\imultisession_put_inuse.htm
tech.root: imapi
ms.assetid: d4eef9de-8b7e-4326-b66f-dddbe2b8a05d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMultisession interface [IMAPI],put_InUse method, IMultisession.put_InUse, IMultisession::put_InUse, imapi.imultisession_put_inuse, imapi2/IMultisession::put_InUse, put_InUse, put_InUse method [IMAPI], put_InUse method [IMAPI],IMultisession interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IMultisession.put_InUse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMultisession::put_InUse


## -description


Determines if this multi-session interface is the one you should use on the current media.


## -parameters




### -param value [in]

Set to VARIANT_TRUE if this multi-session interface is the one you should use to write to the current media. Otherwise, VARIANT_FALSE.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -see-also




<a href="https://msdn.microsoft.com/a983af02-ee0e-4a62-8ae0-fb9a1e0c2571">IMultisession</a>



<a href="https://msdn.microsoft.com/35ebf336-0d67-422c-b6f7-2fd6ee3e7226">IMultisession::get_InUse</a>
 

 

