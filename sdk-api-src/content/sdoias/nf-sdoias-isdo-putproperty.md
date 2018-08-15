---
UID: NF:sdoias.ISdo.PutProperty
title: ISdo::PutProperty
author: windows-sdk-content
description: The PutProperty method sets the value of the specified property.
old-location: nps\SDO_isdo_putproperty.htm
old-project: nps
ms.assetid: c2e440a7-d58c-4542-bd0b-a06b810edd34
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ISdo interface [Network Policy Server],PutProperty method, ISdo.PutProperty, ISdo::PutProperty, PutProperty, PutProperty method [Network Policy Server], PutProperty method [Network Policy Server],ISdo interface, _sdo_isdo_putproperty, nps.SDO_isdo_putproperty, sdo.isdo_putproperty, sdoias/ISdo::PutProperty
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
 - ISdo.PutProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: ADAM
---

# ISdo::PutProperty


## -description


The 
<b>PutProperty</b> method sets the value of the specified property.


## -parameters




### -param Id [in]

Specifies the ID of an existing property.


### -param pValue [in]

Pointer to a 
<a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> that contains the value for that property.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



After you have set values using <b>ISdo::PutProperty</b>, call 
<a href="https://msdn.microsoft.com/aceca2f9-7b17-46a5-bcd1-e6fec3c369ed">ISdo::Apply</a> to write the changes to persistent storage.

The method fails if the property is READ_ONLY or if the value is invalid.




## -see-also




<a href="https://msdn.microsoft.com/9c7ee4d7-987f-45ae-810f-fc310955f36d">IASCOMMONPROPERTIES</a>



<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a>



<a href="https://msdn.microsoft.com/aceca2f9-7b17-46a5-bcd1-e6fec3c369ed">ISdo::Apply</a>



<a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a>
 

 

