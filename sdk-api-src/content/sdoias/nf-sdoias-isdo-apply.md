---
UID: NF:sdoias.ISdo.Apply
title: ISdo::Apply (sdoias.h)
description: The Apply method writes to persistent storage the changes made by calls to the ISdo::PutProperty method.
helpviewer_keywords: ["Apply","Apply method [Network Policy Server]","Apply method [Network Policy Server]","ISdo interface","ISdo interface [Network Policy Server]","Apply method","ISdo.Apply","ISdo::Apply","_sdo_isdo_apply","nps.SDO_isdo_apply","sdo.isdo_apply","sdoias/ISdo::Apply"]
old-location: nps\SDO_isdo_apply.htm
tech.root: Nps
ms.assetid: aceca2f9-7b17-46a5-bcd1-e6fec3c369ed
ms.date: 12/05/2018
ms.keywords: Apply, Apply method [Network Policy Server], Apply method [Network Policy Server],ISdo interface, ISdo interface [Network Policy Server],Apply method, ISdo.Apply, ISdo::Apply, _sdo_isdo_apply, nps.SDO_isdo_apply, sdo.isdo_apply, sdoias/ISdo::Apply
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
 - ISdo::Apply
 - sdoias/ISdo::Apply
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
 - ISdo.Apply
---

# ISdo::Apply


## -description

The 
<b>Apply</b> method writes to persistent storage the changes made by calls to the 
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty">ISdo::PutProperty</a> method.



## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -remarks

To cancel changes made by 
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty">ISdo::PutProperty</a>, call 
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-restore">ISdo::Restore</a>.

## -see-also

<a href="/windows/desktop/api/sdoias/nn-sdoias-isdo">ISdo</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty">ISdo::PutProperty</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-restore">ISdo::Restore</a>
