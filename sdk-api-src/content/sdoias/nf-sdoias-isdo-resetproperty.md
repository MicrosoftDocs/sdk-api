---
UID: NF:sdoias.ISdo.ResetProperty
title: ISdo::ResetProperty (sdoias.h)
description: The ResetProperty method resets the specified property to its default value.
helpviewer_keywords: ["ISdo interface [Network Policy Server]","ResetProperty method","ISdo.ResetProperty","ISdo::ResetProperty","ResetProperty","ResetProperty method [Network Policy Server]","ResetProperty method [Network Policy Server]","ISdo interface","_sdo_isdo_resetproperty","nps.SDO_isdo_resetproperty","sdo.isdo_resetproperty","sdoias/ISdo::ResetProperty"]
old-location: nps\SDO_isdo_resetproperty.htm
tech.root: Nps
ms.assetid: 650df0aa-6331-4a3f-b965-d48fd68fd31d
ms.date: 12/05/2018
ms.keywords: ISdo interface [Network Policy Server],ResetProperty method, ISdo.ResetProperty, ISdo::ResetProperty, ResetProperty, ResetProperty method [Network Policy Server], ResetProperty method [Network Policy Server],ISdo interface, _sdo_isdo_resetproperty, nps.SDO_isdo_resetproperty, sdo.isdo_resetproperty, sdoias/ISdo::ResetProperty
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
 - ISdo::ResetProperty
 - sdoias/ISdo::ResetProperty
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
 - ISdo.ResetProperty
---

# ISdo::ResetProperty


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

<a href="/windows/desktop/api/sdoias/nn-sdoias-isdo">ISdo</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty">ISdo::PutProperty</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-restore">ISdo::Restore</a>