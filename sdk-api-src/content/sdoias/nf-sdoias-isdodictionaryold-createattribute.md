---
UID: NF:sdoias.ISdoDictionaryOld.CreateAttribute
title: ISdoDictionaryOld::CreateAttribute
author: windows-sdk-content
description: The CreateAttribute method creates a new attribute object and returns an IDispatch interface to it.
old-location: nps\SDO_isdodictionaryold_createattribute.htm
old-project: Nps
ms.assetid: 8c5a203b-b60b-4053-b1c4-eca2c30a050e
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CreateAttribute, CreateAttribute method [Network Policy Server], CreateAttribute method [Network Policy Server],ISdoDictionaryOld interface, ISdoDictionaryOld interface [Network Policy Server],CreateAttribute method, ISdoDictionaryOld.CreateAttribute, ISdoDictionaryOld::CreateAttribute, _sdo_isdodictionaryold_createattribute, nps.SDO_isdodictionaryold_createattribute, sdo.isdodictionaryold_createattribute, sdoias/ISdoDictionaryOld::CreateAttribute
ms.prod: windows
ms.technology: windows-sdk
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
 - ISdoDictionaryOld.CreateAttribute
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: ADAM
---

# ISdoDictionaryOld::CreateAttribute


## -description


The 
<b>CreateAttribute</b> method creates a new attribute object and returns an 
<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface to it.


## -parameters




### -param Id [in]

Specifies a value from the enumeration type 
<a href="https://msdn.microsoft.com/42a74deb-6d6e-493a-b9e0-d9549a5530d3">ATTRIBUTEID</a>. This value specifies the type of attribute to create.


### -param ppAttributeObject [out]

Pointer to a pointer to an 
<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer for the created attribute object.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -see-also




<a href="https://msdn.microsoft.com/42a74deb-6d6e-493a-b9e0-d9549a5530d3">ATTRIBUTEID</a>



<a href="https://msdn.microsoft.com/5aaa4008-3b39-4d1d-90db-79631e5bb6b9">ISdoDictionaryOld</a>
 

 

