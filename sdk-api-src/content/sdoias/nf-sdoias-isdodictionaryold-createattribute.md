---
UID: NF:sdoias.ISdoDictionaryOld.CreateAttribute
title: ISdoDictionaryOld::CreateAttribute (sdoias.h)
author: windows-sdk-content
description: The CreateAttribute method creates a new attribute object and returns an IDispatch interface to it.
old-location: nps\SDO_isdodictionaryold_createattribute.htm
tech.root: Nps
ms.assetid: 8c5a203b-b60b-4053-b1c4-eca2c30a050e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateAttribute, CreateAttribute method [Network Policy Server], CreateAttribute method [Network Policy Server],ISdoDictionaryOld interface, ISdoDictionaryOld interface [Network Policy Server],CreateAttribute method, ISdoDictionaryOld.CreateAttribute, ISdoDictionaryOld::CreateAttribute, _sdo_isdodictionaryold_createattribute, nps.SDO_isdodictionaryold_createattribute, sdo.isdodictionaryold_createattribute, sdoias/ISdoDictionaryOld::CreateAttribute
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
 - ISdoDictionaryOld.CreateAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISdoDictionaryOld::CreateAttribute


## -description


The 
<b>CreateAttribute</b> method creates a new attribute object and returns an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface to it.


## -parameters




### -param Id [in]

Specifies a value from the enumeration type 
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/ne-sdoias-_attributeid">ATTRIBUTEID</a>. This value specifies the type of attribute to create.


### -param ppAttributeObject [out]

Pointer to a pointer to an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer for the created attribute object.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/ne-sdoias-_attributeid">ATTRIBUTEID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold">ISdoDictionaryOld</a>
 

 

