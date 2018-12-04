---
UID: NF:sdoias.ISdo.Restore
title: ISdo::Restore
author: windows-sdk-content
description: The Restore method reloads the values of the Server Data Objects (SDO) properties from persistent storage.
old-location: nps\SDO_isdo_restore.htm
tech.root: Nps
ms.assetid: 446b1234-9b65-45dc-bb67-c315c26205dc
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISdo interface [Network Policy Server],Restore method, ISdo.Restore, ISdo::Restore, Restore, Restore method [Network Policy Server], Restore method [Network Policy Server],ISdo interface, _sdo_isdo_restore, nps.SDO_isdo_restore, sdo.isdo_restore, sdoias/ISdo::Restore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Iassdo.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdo.Restore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISdo::Restore


## -description


The 
<b>Restore</b> method reloads the values of the Server Data Objects (SDO) properties from persistent storage.


## -parameters






## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Use the 
<b>Restore</b> method to cancel changes made by calls to the 
<a href="https://msdn.microsoft.com/c2e440a7-d58c-4542-bd0b-a06b810edd34">ISdo::PutProperty</a> method.




## -see-also




<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a>



<a href="https://msdn.microsoft.com/aceca2f9-7b17-46a5-bcd1-e6fec3c369ed">ISdo::Apply</a>



<a href="https://msdn.microsoft.com/c2e440a7-d58c-4542-bd0b-a06b810edd34">ISdo::PutProperty</a>
 

 

