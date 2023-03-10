---
UID: NF:sdoias.ISdo.PutProperty
title: ISdo::PutProperty (sdoias.h)
description: The PutProperty method sets the value of the specified property.
helpviewer_keywords: ["ISdo interface [Network Policy Server]","PutProperty method","ISdo.PutProperty","ISdo::PutProperty","PutProperty","PutProperty method [Network Policy Server]","PutProperty method [Network Policy Server]","ISdo interface","_sdo_isdo_putproperty","nps.SDO_isdo_putproperty","sdo.isdo_putproperty","sdoias/ISdo::PutProperty"]
old-location: nps\SDO_isdo_putproperty.htm
tech.root: Nps
ms.assetid: c2e440a7-d58c-4542-bd0b-a06b810edd34
ms.date: 12/05/2018
ms.keywords: ISdo interface [Network Policy Server],PutProperty method, ISdo.PutProperty, ISdo::PutProperty, PutProperty, PutProperty method [Network Policy Server], PutProperty method [Network Policy Server],ISdo interface, _sdo_isdo_putproperty, nps.SDO_isdo_putproperty, sdo.isdo_putproperty, sdoias/ISdo::PutProperty
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISdo::PutProperty
 - sdoias/ISdo::PutProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdo.PutProperty
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
<a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> that contains the value for that property.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -remarks

After you have set values using <b>ISdo::PutProperty</b>, call 
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-apply">ISdo::Apply</a> to write the changes to persistent storage.

The method fails if the property is READ_ONLY or if the value is invalid.

## -see-also

<a href="/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties">IASCOMMONPROPERTIES</a>



<a href="/windows/desktop/api/sdoias/nn-sdoias-isdo">ISdo</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-apply">ISdo::Apply</a>



<a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>