---
UID: NF:sdoias.ISdo.GetPropertyInfo
title: ISdo::GetPropertyInfo method
author: windows-driver-content
description: The GetPropertyInfo method retrieves a pointer to an ISdoPropertyInfo interface for the specified property.
old-location: nps\SDO_isdo_getpropertyinfo.htm
old-project: Nps
ms.assetid: fa2f0209-ec78-4b59-8f01-f1534b8894c1
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: GetPropertyInfo method [Network Policy Server], GetPropertyInfo method [Network Policy Server], ISdo interface, GetPropertyInfo,ISdo.GetPropertyInfo, ISdo, ISdo interface [Network Policy Server], GetPropertyInfo method, ISdo::GetPropertyInfo, _sdo_isdo_getpropertyinfo, nps.SDO_isdo_getpropertyinfo, sdo.isdo_getpropertyinfo, sdoias/ISdo::GetPropertyInfo
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
-	ISdo.GetPropertyInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISdo::GetPropertyInfo method


## -description


The 
<b>GetPropertyInfo</b> method retrieves a pointer to an <b>ISdoPropertyInfo</b> interface for the specified property.

<b>Warning:  </b>The <b>ISdoPropertyInfo</b> interface is unsupported and the use of this method to access it is discouraged.


## -parameters




### -param Id [in]

Specifies the ID of an existing property.


### -param ppPropertyInfo [out]

Pointer to a pointer that receives the address of an <b>ISdoPropertyInfo</b> interface for the specified property.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Although Server Data Objects (SDO) exposes this method, you do not need it in order to use SDO.




## -see-also




<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a>
 

 

