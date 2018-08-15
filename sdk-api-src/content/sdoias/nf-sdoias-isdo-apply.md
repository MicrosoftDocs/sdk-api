---
UID: NF:sdoias.ISdo.Apply
title: ISdo::Apply
author: windows-sdk-content
description: The Apply method writes to persistent storage the changes made by calls to the ISdo::PutProperty method.
old-location: nps\SDO_isdo_apply.htm
old-project: nps
ms.assetid: aceca2f9-7b17-46a5-bcd1-e6fec3c369ed
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Apply, Apply method [Network Policy Server], Apply method [Network Policy Server],ISdo interface, ISdo interface [Network Policy Server],Apply method, ISdo.Apply, ISdo::Apply, _sdo_isdo_apply, nps.SDO_isdo_apply, sdo.isdo_apply, sdoias/ISdo::Apply
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sdoias.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VENDORPROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdo.Apply
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: ADAM
---

# ISdo::Apply


## -description


The 
<b>Apply</b> method writes to persistent storage the changes made by calls to the 
<a href="https://msdn.microsoft.com/c2e440a7-d58c-4542-bd0b-a06b810edd34">ISdo::PutProperty</a> method.


## -parameters






## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



To cancel changes made by 
<a href="https://msdn.microsoft.com/c2e440a7-d58c-4542-bd0b-a06b810edd34">ISdo::PutProperty</a>, call 
<a href="https://msdn.microsoft.com/446b1234-9b65-45dc-bb67-c315c26205dc">ISdo::Restore</a>.




## -see-also




<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a>



<a href="https://msdn.microsoft.com/c2e440a7-d58c-4542-bd0b-a06b810edd34">ISdo::PutProperty</a>



<a href="https://msdn.microsoft.com/446b1234-9b65-45dc-bb67-c315c26205dc">ISdo::Restore</a>
 

 

