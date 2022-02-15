---
UID: NF:sdoias.ISdo.Restore
title: ISdo::Restore (sdoias.h)
description: The Restore method reloads the values of the Server Data Objects (SDO) properties from persistent storage.
helpviewer_keywords: ["ISdo interface [Network Policy Server]","Restore method","ISdo.Restore","ISdo::Restore","Restore","Restore method [Network Policy Server]","Restore method [Network Policy Server]","ISdo interface","_sdo_isdo_restore","nps.SDO_isdo_restore","sdo.isdo_restore","sdoias/ISdo::Restore"]
old-location: nps\SDO_isdo_restore.htm
tech.root: Nps
ms.assetid: 446b1234-9b65-45dc-bb67-c315c26205dc
ms.date: 12/05/2018
ms.keywords: ISdo interface [Network Policy Server],Restore method, ISdo.Restore, ISdo::Restore, Restore, Restore method [Network Policy Server], Restore method [Network Policy Server],ISdo interface, _sdo_isdo_restore, nps.SDO_isdo_restore, sdo.isdo_restore, sdoias/ISdo::Restore
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
 - ISdo::Restore
 - sdoias/ISdo::Restore
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
 - ISdo.Restore
---

# ISdo::Restore


## -description

The 
<b>Restore</b> method reloads the values of the Server Data Objects (SDO) properties from persistent storage.



## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -remarks

Use the 
<b>Restore</b> method to cancel changes made by calls to the 
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty">ISdo::PutProperty</a> method.

## -see-also

<a href="/windows/desktop/api/sdoias/nn-sdoias-isdo">ISdo</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-apply">ISdo::Apply</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty">ISdo::PutProperty</a>
