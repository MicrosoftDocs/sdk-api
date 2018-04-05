---
UID: NF:sdoias.ISdo.ResetProperty
title: ISdo::ResetProperty method
author: windows-driver-content
description: The ResetProperty method resets the specified property to its default value.
old-location: nps\SDO_isdo_resetproperty.htm
old-project: Nps
ms.assetid: 650df0aa-6331-4a3f-b965-d48fd68fd31d
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: ISdo, ISdo interface [Network Policy Server], ResetProperty method, ISdo::ResetProperty, ResetProperty method [Network Policy Server], ResetProperty method [Network Policy Server], ISdo interface, ResetProperty,ISdo.ResetProperty, _sdo_isdo_resetproperty, nps.SDO_isdo_resetproperty, sdo.isdo_resetproperty, sdoias/ISdo::ResetProperty
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
req.typenames: VENDORPROPERTIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Iassdo.dll
api_name:
-	ISdo.ResetProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ISdo::ResetProperty method


## -description


The 
<b>ResetProperty</b> method resets the specified property to its default value.


## -parameters




### -param Id

Specifies the ID of an existing property.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Very few IAS properties have default values. If you reset a property that does not have a default value, <b>E_INVALIDARG</b> is returned. In Visual Basic, an error similar to the following is returned: "Function call is invalid".

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a>



<a href="https://msdn.microsoft.com/c2e440a7-d58c-4542-bd0b-a06b810edd34">ISdo::PutProperty</a>



<a href="https://msdn.microsoft.com/446b1234-9b65-45dc-bb67-c315c26205dc">ISdo::Restore</a>
 

 

